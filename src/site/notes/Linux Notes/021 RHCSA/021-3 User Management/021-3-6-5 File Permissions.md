---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-3-user-management/021-3-6-5-file-permissions/"}
---

Links : [[Linux Notes/021 RHCSA/021 RHCSA Index\|021 RHCSA Index]]

# File permissions

- All the concept of permissions that we saw for a directory is same for a file as well
- The only difference is that the maximum permission level for a **directory** is **777** while for a **file** is **666**
- All files except program files are called regular files.
- On a regular file, a user can only perform read and write operation
- Hence, on all regular files combination of only read and write is used for all categories 
	<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="021-3-5-5_File_Permissions_2023-09-23_2121.19.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.9.19","elements":[{"type":"text","version":15,"versionNonce":1291922328,"isDeleted":false,"id":"lfZAy9nW","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-223.875,"y":-192.2250213623047,"strokeColor":"#e03131","backgroundColor":"transparent","width":40.99147033691406,"height":35.34483847239366,"seed":1557648360,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1695484589914,"link":null,"locked":false,"fontSize":28.27587077791493,"fontFamily":1,"text":"rw-","rawText":"rw-","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"rw-","lineHeight":1.25,"baseline":25},{"type":"text","version":55,"versionNonce":1594064104,"isDeleted":false,"id":"Up3ONEVa","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-180.2750244140625,"y":-191.6250762939453,"strokeColor":"#1971c2","backgroundColor":"transparent","width":36.19197082519531,"height":31.206966223319448,"seed":1307690472,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1695484595882,"link":null,"locked":false,"fontSize":24.96557297865556,"fontFamily":1,"text":"rw-","rawText":"rw-","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"rw-","lineHeight":1.25,"baseline":22},{"type":"text","version":74,"versionNonce":1915007640,"isDeleted":false,"id":"qCnfWuHe","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-141.875,"y":-192.8250274658203,"strokeColor":"#2f9e44","backgroundColor":"transparent","width":39.396484375,"height":33.965442489563486,"seed":1399732200,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1695484599937,"link":null,"locked":false,"fontSize":27.17235399165079,"fontFamily":1,"text":"rw-","rawText":"rw-","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"rw-","lineHeight":1.25,"baseline":23},{"type":"line","version":219,"versionNonce":921310104,"isDeleted":false,"id":"T4g3fmyklwAMfumpetwj2","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":1.5721350904939824,"x":-210.317037439576,"y":-173.9385025537648,"strokeColor":"#e03131","backgroundColor":"transparent","width":13.633424760715776,"height":33.57438991419212,"seed":1352798440,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1695484618298,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[5.964668026704972,0],[6.390673951207132,16.057318529549676],[13.633424760715776,16.057318529549676],[5.112526159106268,16.057318529549676],[6.390673951207132,33.57438991419212],[1.7042187259002175,33.57438991419212]]},{"type":"line","version":250,"versionNonce":2077944984,"isDeleted":false,"id":"XYg6OL9S87NYgb8qX6K1m","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":1.5721350904939824,"x":-127.29207434445368,"y":-174.68697432665903,"strokeColor":"#2f9e44","backgroundColor":"transparent","width":13.633424760715776,"height":33.57438991419212,"seed":663157992,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1695484608226,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[5.964668026704972,0],[6.390673951207132,16.057318529549676],[13.633424760715776,16.057318529549676],[5.112526159106268,16.057318529549676],[6.390673951207132,33.57438991419212],[1.7042187259002175,33.57438991419212]]},{"type":"line","version":261,"versionNonce":498101224,"isDeleted":false,"id":"c2ivB0dGyTG3qCLoBvRfm","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":1.5721350904939824,"x":-168.87248161895255,"y":-173.53497835508256,"strokeColor":"#1971c2","backgroundColor":"transparent","width":13.633424760715776,"height":33.57438991419212,"seed":91692952,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1695484612986,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[5.964668026704972,0],[6.390673951207132,16.057318529549676],[13.633424760715776,16.057318529549676],[5.112526159106268,16.057318529549676],[6.390673951207132,33.57438991419212],[1.7042187259002175,33.57438991419212]]},{"type":"text","version":20,"versionNonce":866381464,"isDeleted":false,"id":"tq8Q9LqA","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-209.875,"y":-151.8250274658203,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":11.3599853515625,"height":25,"seed":507218072,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1695484394342,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"u","rawText":"u","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"u","lineHeight":1.25,"baseline":18},{"type":"text","version":26,"versionNonce":5051288,"isDeleted":false,"id":"prbV9zxc","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-165.875,"y":-152.62501525878906,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":10.019989013671875,"height":25,"seed":123681000,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1695484397107,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"g","rawText":"g","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"g","lineHeight":1.25,"baseline":18},{"type":"text","version":53,"versionNonce":681111784,"isDeleted":false,"id":"JtHV6QLp","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-122.875,"y":-149.8250274658203,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":11.079986572265625,"height":25,"seed":808295832,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1695484404603,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"o","rawText":"o","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"o","lineHeight":1.25,"baseline":18},{"type":"text","version":182,"versionNonce":1008403608,"isDeleted":false,"id":"c9DXmKUC","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":106.52490234375,"y":-182.8250274658203,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":301.6398010253906,"height":50,"seed":1411693032,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1695484487219,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"umask of root       ==> 022\numask of local user  ==> 002","rawText":"umask of root       ==> 022\numask of local user  ==> 002","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"umask of root       ==> 022\numask of local user  ==> 002","lineHeight":1.25,"baseline":43}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#e03131","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":244.74704020732156,"scrollY":355.6763887147646,"zoom":{"value":1.85},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("021-3-5-5_File_Permissions_2023-09-23_2121.19.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>
- Formula to calculate default permission is **maximum permission level - umask**
- maximum permission level for file is **666**
- In case of root creating a file :
	==666 - 022 = 644==   rw-r--r--
- In case of local user creating a file :
	==666- 022 =664==   rw-rw-r--