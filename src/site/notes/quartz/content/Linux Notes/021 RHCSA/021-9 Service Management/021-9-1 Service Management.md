---
{"dg-publish":true,"permalink":"/quartz/content/linux-notes/021-rhcsa/021-9-service-management/021-9-1-service-management/","noteIcon":"","created":"2023-10-14T22:10:59.674+05:30","updated":"2023-10-13T17:09:52.485+05:30"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Service Management


- **A service is a script** that is responsible to start, stop or restart process of a program
- All service files are stored in `/usr/lib/systemd/system` directory
	- If your server is running with **[[init\|init]]** program, `service` command is used to manage services
- If your server is running with **[[process continuation 2#^803dfd\|systemd]]** program, `systemctl` command is used to manage services
- Services can be started, stopped or restarted in run time
- We can also enable a service to start automatically when server boots

<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="021-9_Service_Management_2023-10-06_1634.40.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.9.19","elements":[{"id":"aqeVA6M3","type":"text","x":-188.83447265625,"y":-204.7976837158203,"width":33.95997619628906,"height":175,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":543658543,"version":30,"versionNonce":1180438689,"isDeleted":false,"boundElements":null,"updated":1696590308093,"link":null,"locked":false,"text":"2.0\n2.2\n2.4\n2.6\n3.x\n4.x\n5.x","rawText":"2.0\n2.2\n2.4\n2.6\n3.x\n4.x\n5.x","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":167,"containerId":null,"originalText":"2.0\n2.2\n2.4\n2.6\n3.x\n4.x\n5.x","lineHeight":1.25},{"id":"qGWR2VYayKbelPq__Tr1F","type":"line","x":-141.11389160156247,"y":-201.24009704589844,"width":48.1995849609375,"height":86.75924682617188,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1261902945,"version":144,"versionNonce":691158959,"isDeleted":false,"boundElements":null,"updated":1696590349230,"link":null,"locked":false,"points":[[0,0],[32.4251708984375,0],[28.9197998046875,44.694183349609375],[48.1995849609375,45.570526123046875],[28.04345703125,50.82867431640625],[29.796142578125,81.50112915039062],[1.752685546875,86.75924682617188]],"lastCommittedPoint":[1.752685546875,86.75924682617188],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"type":"line","version":184,"versionNonce":184338319,"isDeleted":false,"id":"GJe6aM_Rx-Uip6c_KTKlv","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-140.41525461775484,"y":-92.75205572255497,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":33.29989984147651,"height":56.394305424375,"seed":1358320609,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1696590341584,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[22.4017477357076,0],[19.979973639028497,29.051628716428084],[33.29989984147651,29.621259549216386],[20.585417163198272,30.76054105149841],[20.585417163198272,52.976480754234345],[1.2108870483395502,56.394305424375005]]},{"id":"0Uhiq34k","type":"text","x":-76.8560791015625,"y":-169.31394958496094,"width":29.39996337890625,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":1581128321,"version":18,"versionNonce":201640001,"isDeleted":false,"boundElements":null,"updated":1696590364452,"link":null,"locked":false,"text":"init","rawText":"init","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":17,"containerId":null,"originalText":"init","lineHeight":1.25},{"id":"zXwiZY88","type":"text","x":-97.0123291015625,"y":-78.20115661621094,"width":77.37991333007812,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":173621487,"version":27,"versionNonce":395310191,"isDeleted":false,"boundElements":null,"updated":1696590362652,"link":null,"locked":false,"text":"systemd","rawText":"systemd","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":17,"containerId":null,"originalText":"systemd","lineHeight":1.25}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":347.78326416015625,"scrollY":402.5692138671875,"zoom":{"value":1},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("021-9_Service_Management_2023-10-06_1634.40.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

<hr>

## Commands

&rarr; To list all active services
`systemctl list-units --type=service`

&rarr; To list installed services 
`systemctl list-units --type=service --all`

&rarr; To check status of a service 
`systemctl status crond`

&rarr; To stop a service
`systemctl stop crond`

&rarr; To start a service
`systemctl start crond`

&rarr; To restart a service
`systemctl restart crond`

&rarr; <abbr title="A masked service cannot be started or enabled">To mask a service</abbr>
`systemctl mask crond`

&rarr; To unmask a service
`systemctl unmask crond`

&rarr; To enable a service at every system boot
`systemctl enable --now crond`

&rarr; To disable a service at every system boot
`systemctl disable --now crond`

<hr>

>[!Note]
You can use these commands with any services you want I have showed example of **crond** service




