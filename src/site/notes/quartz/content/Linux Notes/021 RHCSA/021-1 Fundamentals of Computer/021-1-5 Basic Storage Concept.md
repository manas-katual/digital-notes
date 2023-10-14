---
{"dg-publish":true,"permalink":"/quartz/content/linux-notes/021-rhcsa/021-1-fundamentals-of-computer/021-1-5-basic-storage-concept/","noteIcon":"","created":"2023-10-14T22:10:59.506+05:30","updated":"2023-10-14T17:28:25.085+05:30"}
---

Link : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Storage

- Data is stored physically on hard drives and other storage devices
- We need to access data logically from storage device via operating system 
- Every operating system has a logical access point to access storage devices
- This access points are called mount points
- In windows operating system, mount points are in the form of drive letters

<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="Basic_Storage_Conceptexcalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.9.19","elements":[{"type":"text","version":33,"versionNonce":935478784,"isDeleted":false,"id":"XMf4D9XY","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-192.33331298828125,"y":-136.16146850585938,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":73.25997924804688,"height":50,"seed":209132032,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694768923277,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"100 GB\n  C :","rawText":"100 GB\n  C :","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"100 GB\n  C :","lineHeight":1.25,"baseline":42},{"type":"text","version":50,"versionNonce":1930123776,"isDeleted":false,"id":"ZFWAgZzk","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-83.3333740234375,"y":-131.16143798828125,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":82.07997131347656,"height":50,"seed":245766656,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694768925532,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"200 GB\n   D :","rawText":"200 GB\n   D :","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"200 GB\n   D :","lineHeight":1.25,"baseline":42},{"type":"text","version":60,"versionNonce":2083325440,"isDeleted":false,"id":"9je83dfs","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":31.6666259765625,"y":-132.16143798828125,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":80.63996887207031,"height":50,"seed":82663936,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694768927444,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"400 GB\n   E :","rawText":"400 GB\n   E :","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"400 GB\n   E :","lineHeight":1.25,"baseline":42},{"type":"text","version":48,"versionNonce":204773888,"isDeleted":false,"id":"kOER8Ynm","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":141,"y":-134.16146850585938,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":69.35997009277344,"height":50,"seed":480025088,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694768929381,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"4.7 GB\n   F :","rawText":"4.7 GB\n   F :","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"4.7 GB\n   F :","lineHeight":1.25,"baseline":42},{"type":"text","version":35,"versionNonce":674219520,"isDeleted":false,"id":"bza6zkvK","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":243.5098517922794,"y":-135.55360322840073,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":55.61997985839844,"height":50,"seed":117791232,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694768932301,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"8 GB\n  G :","rawText":"8 GB\n  G :","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"8 GB\n  G :","lineHeight":1.25,"baseline":42},{"type":"line","version":122,"versionNonce":1443825152,"isDeleted":false,"id":"q0IN5XEZpHSbrPp6JGuxH","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-102.6665541704963,"y":-140.62129121668215,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":0,"height":35.137277042164555,"seed":754402816,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1694766100645,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[0,35.137277042164555]]},{"type":"line","version":73,"versionNonce":1493473792,"isDeleted":false,"id":"PwcAXoW7M-ijwfDPXzEEz","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":16.862792968750057,"y":-143.7193388097428,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":0.6666259765625,"height":32.58823529411768,"seed":1655331328,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1694766104341,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[-0.6666259765625,32.58823529411768]]},{"type":"line","version":118,"versionNonce":2129238528,"isDeleted":false,"id":"6tcgWGlAh2VN2aR-PiErc","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":124.62762810202213,"y":-144.62132173426028,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":0.8629150390625,"height":36.03922406364893,"seed":1016448512,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1694766126479,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[-0.8629150390625,36.03922406364893]]},{"type":"line","version":69,"versionNonce":1465976320,"isDeleted":false,"id":"3x1Y_qM9EGGuV1t1BxFuT","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":226.27455767463243,"y":-147.64091940487148,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":1.6863151999081083,"height":33.96080465877762,"seed":1342069248,"groupIds":[],"frameId":null,"roundness":{"type":2},"boundElements":[],"updated":1694766121516,"link":null,"locked":false,"startBinding":null,"endBinding":null,"lastCommittedPoint":null,"startArrowhead":null,"endArrowhead":null,"points":[[0,0],[-1.6863151999081083,33.96080465877762]]}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":211.7299457970068,"scrollY":267.03835256583073,"zoom":{"value":1.9500000000000002},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Basic_Storage_Conceptexcalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

- Linux does not support drive letters
- In Linux empty directories can be used as mount points

<div id="Basic_Storage_Concept_2excalidraw.md2"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.9.19","elements":[{"id":"Mq1ZSnZF","type":"text","x":-215,"y":-123.828125,"width":73.25997924804688,"height":50,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":213211648,"version":45,"versionNonce":1136515584,"isDeleted":false,"boundElements":null,"updated":1694766459225,"link":null,"locked":false,"text":"100 GB\n  dir 1","rawText":"100 GB\n  dir 1","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":42,"containerId":null,"originalText":"100 GB\n  dir 1","lineHeight":1.25},{"id":"Rnd0JLFN","type":"text","x":-111,"y":-122.16143798828125,"width":82.07997131347656,"height":50,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":1363646976,"version":59,"versionNonce":1550981632,"isDeleted":false,"boundElements":null,"updated":1694766461422,"link":null,"locked":false,"text":"200 GB\n  dir 2","rawText":"200 GB\n  dir 2","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":42,"containerId":null,"originalText":"200 GB\n  dir 2","lineHeight":1.25},{"id":"lUornj84","type":"text","x":-2.6666259765625,"y":-117.828125,"width":80.63996887207031,"height":50,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":260168192,"version":66,"versionNonce":909711872,"isDeleted":false,"boundElements":null,"updated":1694766465737,"link":null,"locked":false,"text":"400 GB\n  dir 3","rawText":"400 GB\n  dir 3","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":42,"containerId":null,"originalText":"400 GB\n  dir 3","lineHeight":1.25},{"id":"SioPewMp","type":"text","x":94,"y":-115.828125,"width":69.35997009277344,"height":50,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":683842048,"version":53,"versionNonce":242375168,"isDeleted":false,"boundElements":null,"updated":1694766469285,"link":null,"locked":false,"text":"4.7 GB\n  dir 4","rawText":"4.7 GB\n  dir 4","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":42,"containerId":null,"originalText":"4.7 GB\n  dir 4","lineHeight":1.25},{"id":"08MOWcl8","type":"text","x":179,"y":-116.49478149414062,"width":56.71995544433594,"height":50,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":309025280,"version":51,"versionNonce":678725120,"isDeleted":false,"boundElements":null,"updated":1694766474192,"link":null,"locked":false,"text":"8 GB\n dir 5","rawText":"8 GB\n dir 5","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":42,"containerId":null,"originalText":"8 GB\n dir 5","lineHeight":1.25},{"id":"foVfH0YglawXTESpqrlrM","type":"line","x":-127,"y":-126.16145324707031,"width":0.6666259765625,"height":29.333328247070312,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":227214848,"version":23,"versionNonce":824449536,"isDeleted":false,"boundElements":null,"updated":1694766483127,"link":null,"locked":false,"points":[[0,0],[-0.6666259765625,29.333328247070312]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"mwW1Ue1BXsXJWJdjJc9lj","type":"line","x":-16.33331298828125,"y":-124.828125,"width":0,"height":30,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1771100672,"version":19,"versionNonce":1779238400,"isDeleted":false,"boundElements":null,"updated":1694766487125,"link":null,"locked":false,"points":[[0,0],[0,30]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"sSqe-hSPDXA28twi2HBkj","type":"line","x":89,"y":-121.49478149414062,"width":0.6666259765625,"height":35.333343505859375,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1853638144,"version":26,"versionNonce":539302400,"isDeleted":false,"boundElements":null,"updated":1694766492157,"link":null,"locked":false,"points":[[0,0],[-0.6666259765625,35.333343505859375]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"BpZtNpFocK5Uni8XCcg3T","type":"line","x":167.666748046875,"y":-119.49478149414062,"width":2.6666259765625,"height":40.666656494140625,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":1349638656,"version":33,"versionNonce":507086336,"isDeleted":false,"boundElements":null,"updated":1694766498390,"link":null,"locked":false,"points":[[0,0],[2.6666259765625,40.666656494140625]],"lastCommittedPoint":null,"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":258,"scrollY":297.171875,"zoom":{"value":1},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Basic_Storage_Concept_2excalidraw.md2");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

- When we install operating system on a hard drive, a default directory structure gets created that contains various system files and can also be used to store user data.
- This default directory structure is called a file system.
- Windows file system start from **C: drive** and contains directories like windows, program files and users
- Since there is no drive letter support in Linux, Linux directory structure starts from a directory called slash directory **"/"** 
- **"/"** is the root directory of Linux file system.
- All other files & directories always fall inside **"/"** directory.
- Various Linux directories that fall directly under **"/"** directory include [[Linux Notes/021 RHCSA/021-2 FIle Management/021-2-1 File System#^3f0f81\|boot]], [[021-2 File Management#^3a09c4\|dev]], [[021-2 File Management#^21fa6c\|var]], [[021-2 File Management#^2a7a7d\|usr]], [[021-2 File Management#^8accbb\|lib]], [[021-2 File Management#^c3f9f7\|etc]], [[021-2 File Management#^5df4b4\|proc]], [[021-2 File Management#^19ef98\|home]], [[021-2 File Management#^3ad100\|root]], and [[021-2 File Management#^3be19b\|tmp]]

==for better understanding see below diagram==

<div id="Basic_Storage_Concept_3excalidraw.md3"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.9.19","elements":[{"type":"text","version":48,"versionNonce":35003622,"isDeleted":false,"id":"Kz2A4f2E","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-152,"y":-609.828125,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":43.61994934082031,"height":175,"seed":48039424,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694851858623,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"boot\ndev\nvar\nusr\nlib\netc\nproc","rawText":"boot\ndev\nvar\nusr\nlib\netc\nproc","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"boot\ndev\nvar\nusr\nlib\netc\nproc","lineHeight":1.25,"baseline":167},{"type":"freedraw","version":119,"versionNonce":2123176448,"isDeleted":false,"id":"9hl8-OUsgCBeghG8jxykE","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-74.33331298828125,"y":-602.828125,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":46,"height":163.33334350585938,"seed":474700288,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694766850272,"link":null,"locked":false,"points":[[0,0],[0,-0.666656494140625],[2.66668701171875,-0.666656494140625],[9.33331298828125,0],[16.66668701171875,1.333343505859375],[17.33331298828125,2],[20.66668701171875,4],[23.33331298828125,6.6666717529296875],[24.66668701171875,9.333343505859375],[28.66668701171875,14],[31.33331298828125,17.333343505859375],[32,19.333343505859375],[33.33331298828125,22.666671752929688],[33.33331298828125,26],[34,28],[34,31.333343505859375],[34,34],[34,36.66668701171875],[34,39.333343505859375],[33.33331298828125,41.333343505859375],[32,44.66668701171875],[30,48.66668701171875],[29.33331298828125,50.66668701171875],[28.66668701171875,52],[27.33331298828125,53.333343505859375],[26,56],[24.66668701171875,57.333343505859375],[23.33331298828125,59.333343505859375],[21.33331298828125,62],[20,62.66668701171875],[20,63.333343505859375],[19.33331298828125,65.33334350585938],[18,66],[17.33331298828125,68],[17.33331298828125,69.33334350585938],[17.33331298828125,70],[17.33331298828125,71.33334350585938],[17.33331298828125,72],[17.33331298828125,72.66668701171875],[17.33331298828125,74],[18.66668701171875,75.33334350585938],[20,75.33334350585938],[22.66668701171875,75.33334350585938],[23.33331298828125,75.33334350585938],[25.33331298828125,75.33334350585938],[26.66668701171875,75.33334350585938],[28.66668701171875,75.33334350585938],[30,74.66668701171875],[30,74],[32.66668701171875,72.66668701171875],[35.33331298828125,70.66668701171875],[36,70],[36.66668701171875,69.33334350585938],[37.33331298828125,68.66668701171875],[37.33331298828125,68],[37.33331298828125,65.33334350585938],[37.33331298828125,64.66668701171875],[37.33331298828125,63.333343505859375],[37.33331298828125,62.66668701171875],[37.33331298828125,63.333343505859375],[37.33331298828125,66],[38.66668701171875,70],[38.66668701171875,75.33334350585938],[39.33331298828125,78.66668701171875],[40,81.33334350585938],[40,82.66668701171875],[40,83.33334350585938],[40.66668701171875,86],[40.66668701171875,89.33334350585938],[42,92.66668701171875],[42,96],[42.66668701171875,100.66668701171875],[43.33331298828125,104],[43.33331298828125,107.33334350585938],[44,110.66668701171875],[44,114.66668701171875],[44,120],[44,122],[45.33331298828125,124],[45.33331298828125,124.66668701171875],[45.33331298828125,126.66668701171875],[45.33331298828125,128],[45.33331298828125,131.33334350585938],[45.33331298828125,133.33334350585938],[44.66668701171875,134.66668701171875],[43.33331298828125,138],[42,140.66668701171875],[41.33331298828125,141.33334350585938],[39.33331298828125,142],[38.66668701171875,144],[37.33331298828125,146.66668701171875],[36,148],[33.33331298828125,150],[30.66668701171875,151.33334350585938],[29.33331298828125,152.66668701171875],[28,154],[26,155.33334350585938],[25.33331298828125,156],[23.33331298828125,157.33334350585938],[21.33331298828125,159.33334350585938],[20,160],[19.33331298828125,160],[18,160],[17.33331298828125,160.66668701171875],[16.66668701171875,160.66668701171875],[14.66668701171875,162],[13.33331298828125,162],[10.66668701171875,162.66668701171875],[8.66668701171875,162.66668701171875],[7.33331298828125,162.66668701171875],[5.33331298828125,162.66668701171875],[4.66668701171875,162.66668701171875],[2,162.66668701171875],[1.33331298828125,162.66668701171875],[-0.66668701171875,162.66668701171875],[-0.66668701171875,162.66668701171875]],"lastCommittedPoint":null,"simulatePressure":true,"pressures":[]},{"type":"text","version":86,"versionNonce":78038528,"isDeleted":false,"id":"dJV7n1Kd","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-0.3333740234375,"y":-550.4947814941406,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":184.01980590820312,"height":25,"seed":465569280,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694766880581,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"System Directories","rawText":"System Directories","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"System Directories","lineHeight":1.25,"baseline":17},{"type":"text","version":72,"versionNonce":390601216,"isDeleted":false,"id":"jmp1wIvC","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-150,"y":-416.1614685058594,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":44.55995178222656,"height":75,"seed":269731328,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694768812730,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"home\nroot\ntmp","rawText":"home\nroot\ntmp","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"home\nroot\ntmp","lineHeight":1.25,"baseline":67},{"type":"freedraw","version":127,"versionNonce":413550080,"isDeleted":false,"id":"0MysWyNjjrswcRhxZ1QPO","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-88.33343505859375,"y":-406.8280944824219,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":19.3333740234375,"height":72.66665649414062,"seed":575363584,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694768816219,"link":null,"locked":false,"points":[[0,0],[2,0],[2,2],[2.66668701171875,3.33331298828125],[2.66668701171875,7.33331298828125],[3.3333740234375,10.666656494140625],[4,14],[4,16.666656494140625],[4,17.33331298828125],[4,19.33331298828125],[4,20],[4,21.33331298828125],[4.66668701171875,22.666656494140625],[4.66668701171875,23.33331298828125],[4.66668701171875,24.666656494140625],[5.3333740234375,26],[6,26],[6,27.33331298828125],[6.66668701171875,28],[7.3333740234375,28],[8,28.666656494140625],[8.66668701171875,28.666656494140625],[10,28.666656494140625],[10.66668701171875,28.666656494140625],[12.66668701171875,28.666656494140625],[13.3333740234375,28.666656494140625],[14,28],[14.66668701171875,27.33331298828125],[16,26.666656494140625],[17.3333740234375,26],[18,25.33331298828125],[18.66668701171875,24.666656494140625],[18.66668701171875,23.33331298828125],[18.66668701171875,24.666656494140625],[18.66668701171875,27.33331298828125],[18.66668701171875,29.33331298828125],[17.3333740234375,32],[17.3333740234375,32.666656494140625],[17.3333740234375,34],[17.3333740234375,35.33331298828125],[17.3333740234375,37.33331298828125],[17.3333740234375,38.666656494140625],[18,39.33331298828125],[18,40.666656494140625],[18,42.666656494140625],[18,44],[18,45.33331298828125],[18,46.666656494140625],[18,48],[19.3333740234375,49.33331298828125],[19.3333740234375,50],[19.3333740234375,51.33331298828125],[19.3333740234375,52],[19.3333740234375,53.33331298828125],[19.3333740234375,54.666656494140625],[19.3333740234375,55.33331298828125],[19.3333740234375,56],[19.3333740234375,58],[19.3333740234375,58.666656494140625],[19.3333740234375,60],[19.3333740234375,60.666656494140625],[19.3333740234375,61.33331298828125],[19.3333740234375,62],[19.3333740234375,63.33331298828125],[18.66668701171875,63.33331298828125],[18.66668701171875,64],[17.3333740234375,65.33331298828125],[16.66668701171875,66],[16,66.66665649414062],[15.3333740234375,66.66665649414062],[14,67.33331298828125],[13.3333740234375,68],[10.66668701171875,69.33331298828125],[9.3333740234375,70],[8.66668701171875,70],[8,70.66665649414062],[7.3333740234375,70.66665649414062],[6,71.33331298828125],[5.3333740234375,71.33331298828125],[4,72],[3.3333740234375,72.66665649414062],[2.66668701171875,72.66665649414062],[2,72.66665649414062],[2,72.66665649414062]],"lastCommittedPoint":null,"simulatePressure":true,"pressures":[]},{"type":"text","version":56,"versionNonce":1562843648,"isDeleted":false,"id":"WGdyHg3t","fillStyle":"hachure","strokeWidth":0.5,"strokeStyle":"solid","roughness":1,"opacity":100,"angle":0,"x":-24,"y":-391.16143798828125,"strokeColor":"#1e1e1e","backgroundColor":"transparent","width":170.2998504638672,"height":25,"seed":347855360,"groupIds":[],"frameId":null,"roundness":null,"boundElements":[],"updated":1694768819518,"link":null,"locked":false,"fontSize":20,"fontFamily":1,"text":"Data Directories","rawText":"Data Directories","textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"Data Directories","lineHeight":1.25,"baseline":17}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":0.5,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":"triangle","currentItemEndArrowhead":"triangle","scrollX":231.7817840576172,"scrollY":620.5807189941406,"zoom":{"value":2},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Basic_Storage_Concept_3excalidraw.md3");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>