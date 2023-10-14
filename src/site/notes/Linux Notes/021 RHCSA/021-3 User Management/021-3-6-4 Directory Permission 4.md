---
{"dg-publish":true,"permalink":"/linux-notes/021-rhcsa/021-3-user-management/021-3-6-4-directory-permission-4/"}
---

Links : [[Linux Notes/021 RHCSA Index\|021 RHCSA Index]]

# Directory Permission 4

### Permissions to numbers :

- read &rarr; 4
- write &rarr; 2
- execute &rarr; 1

### Permissions to permission level :

- rwx &rarr; 421 &rarr; 4+2+1 &rarr; 7
- r-x &rarr; 401 &rarr; 4+0+1 &rarr; 5
- --x &rarr; 001 &rarr; 0+0+1 &rarr; 1

**e.g.**

1. rwxrwxrwx &rarr; 421421421 &rarr; 4+2+1 4+2+1 4+2+1 &rarr; 777 &rarr; maximum permission level
2. rwxr-xr-x &rarr; 421401401 &rarr; 4+2+1 4+0+1 4+0+1 &rarr; 755
3. r-x--x--- &rarr; 401001000 &rarr; 4+0+1 1+0+0 0+0+0 &rarr; 510

---

## Umask
- When root creates a directory, the default permission is **rwxr-xr-x (755)**
- When local users create a directory, then default permission is **rwxrwxr-x (755)**
- The default permission is calculated using **umask**
- **umask** is a number used to calculate default permission

<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="021-3-5-4_Directory_Permission_4_2023-09-23_2057.58.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.9.19","elements":[{"id":"j7a4RrRV","type":"text","x":-199.875,"y":-237.2250213623047,"width":341.6398010253906,"height":50,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":495557352,"version":71,"versionNonce":959797480,"isDeleted":false,"boundElements":null,"updated":1695482970179,"link":null,"locked":false,"text":"umask of root        ==>    022\numask of local user   ==>    002","rawText":"umask of root        ==>    022\numask of local user   ==>    002","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":43,"containerId":null,"originalText":"umask of root        ==>    022\numask of local user   ==>    002","lineHeight":1.25},{"id":"lgjUvit8yr80py0pB9zi8","type":"line","x":145.7249755859375,"y":-227.40418056759177,"width":24.81637903558414,"height":28.82514744609198,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":{"type":2},"seed":437403368,"version":132,"versionNonce":1635455976,"isDeleted":false,"boundElements":null,"updated":1695483003201,"link":null,"locked":false,"points":[[0,0],[15.571148707119178,0.4969777827739134],[16.057626450014546,14.412573723045988],[24.81637903558414,14.909560985063488],[17.030878930764313,14.909560985063488],[17.517430922399438,28.328160184074477],[5.352591649164687,28.825147446091975]],"lastCommittedPoint":[8.800048828125,46.399993896484375],"startBinding":null,"endBinding":null,"startArrowhead":null,"endArrowhead":null},{"id":"UoXeBXSn","type":"text","x":183.3250732421875,"y":-224.8250274658203,"width":105.69987487792969,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"hachure","strokeWidth":1,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":null,"roundness":null,"seed":1081457896,"version":49,"versionNonce":1946182120,"isDeleted":false,"boundElements":null,"updated":1695483026066,"link":null,"locked":false,"text":"pre-defined","rawText":"pre-defined","fontSize":20,"fontFamily":1,"textAlign":"left","verticalAlign":"top","baseline":18,"containerId":null,"originalText":"pre-defined","lineHeight":1.25}],"appState":{"theme":"dark","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"hachure","currentItemStrokeWidth":1,"currentItemStrokeStyle":"solid","currentItemRoughness":1,"currentItemOpacity":100,"currentItemFontFamily":1,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","scrollX":311.125,"scrollY":364.1750183105469,"zoom":{"value":1},"currentItemRoundness":"round","gridSize":null,"gridColor":{"Bold":"#C9C9C9FF","Regular":"#EDEDEDFF"},"currentStrokeOptions":null,"previousGridSize":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("021-3-5-4_Directory_Permission_4_2023-09-23_2057.58.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>

- **Formula** to calculate default permission is **maximum permission level - umask**
- Maximum permission level for directory is **777**
- In case of root creating a directory
	==777 - 022 = 755==
- In case of local user creating a directory 
	==777 - 022 = 775==
- To check current umask of a user :
	`# umask`
- To change umask of a user
	`# umask 027`  (temporary) every user can change its umask

==Umask set using umask command is not persistent. To set umask persistently you have edit .bashrc file==

---

- chmod command is used to change category permissions of a directory
- There are 2 methods of using chmod command
	1. numeric &rarr; permissions are set using permission level
	2. alphabetic &rarr; permissions are set using alphabets
- If we want to apply rwxr-x--x  permission on /data directory using numeric method, then the command would be chmod 751 /data
- If we want to allow write access for others on /data directory using alphabetic method, then the command would be chmod o+w /data ==here o stands for other and w stands for write==
- If we want to allow write access for others and remove access for group on /data directory using alphabetic method, then the command would be chmod o+w,g-r /data **"(+ allow) (- deny)"**
