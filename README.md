# Useful_Library_List
My best used libraries and usage guides











#  [SheetJS](https://sheetjs.com/)

> The SheetJS Community Edition offers battle-tested open-source solutions for extracting useful data from almost any complex spreadsheet and generating new spreadsheets that will work with legacy and modern software alike.

`npm i xlsx `

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
