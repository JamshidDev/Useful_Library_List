# Useful_Library_List
My best used libraries and usage guides











#  [SheetJS](https://sheetjs.com/)

> Excel file reader in Nodejs

`npm i xlsx ` [more](https://www.npmjs.com/package/xlsx)

```javascript
const xlsx_reader = require('xlsx');

const path ="file path....";

const workbook = xlsx_reader.readFile(path);
    let workbook_sheet = workbook.SheetNames;
    let workbook_response = xlsx_reader.utils.sheet_to_json(
        workbook.Sheets[workbook_sheet[0]]
    );

console.log(workbook_response);


  
```
