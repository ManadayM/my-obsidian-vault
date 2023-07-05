/*
![](https://raw.githubusercontent.com/zsviczian/obsidian-excalidraw-plugin/master/images/scripts-stroke-width.jpg)

This script will set the stroke width of selected elements. This is helpful, for example, when you scale freedraw sketches and want to reduce or increase their line width.

See documentation for more details:
https://zsviczian.github.io/obsidian-excalidraw-plugin/ExcalidrawScriptsEngine.html

```javascript
*/
let width = (ea.getViewSelectedElement().strokeWidth??1).toString();
width = await utils.inputPrompt("Width?","number",width);
const elements=ea.getViewSelectedElements();
ea.copyViewElementsToEAforEditing(elements);
ea.getElements().forEach((el)=>el.strokeWidth=width);
ea.addElementsToView(false,false);


## Points

### <font color="darkgreen">DOs</font> ✅
- <font color="green">The goal is to a make useful and impressive-looking summary sales dashboard.</font>
- Keep the images for Dr. von Brunswick's Chocolate Factory, Salesforce, and Coefficient somewhere on your final Dashboard.
	- =IMAGE("https://2nfwi926ajabz80xg2wqec71-wpengine.netdna-ssl.com/wp-content/uploads/2022/06/sgc_icon.png",1)
	- =IMAGE("https://c1.sfdcstatic.com/content/dam/sfdc-docs/www/logos/logo-salesforce.svg")
	- =IMAGE("https://coefficient.io/wp-content/uploads/2022/04/powered-by-coefficient-2x-white.png")
- Use the "⚙️ Settings" tab for any additional lookup tables or reference cells you need.
- Participants are encouraged to make **creative use of Google Sheets** functionalities including, but not limited to, **Data Validations, Advanced Formulas, Conditional Formatting, People Chips, Sparklines, Charts, Pivot Tables, Filter Views, and Slicers**.

### <font color="red">Don't</font> ✋
- The use of Google Apps Script (GAS) or any third-party add-ons is not allowed.