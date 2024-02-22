# Useful_Library_List
My best used libraries and usage guides











#  1.[SheetJS](https://sheetjs.com/)

> Excel file reader in Nodejs

`npm i xlsx ` [more](https://www.npmjs.com/package/xlsx)

```javascript
const xlsx_reader = require('xlsx');

const path ="paht of file....";

const workbook = xlsx_reader.readFile(path);
    let workbook_sheet = workbook.SheetNames;
    let workbook_response = xlsx_reader.utils.sheet_to_json(
        workbook.Sheets[workbook_sheet[0]]
    );

console.log(workbook_response);

```



#  2.[ExcelJS](https://github.com/exceljs/exceljs#readme)

> Excel file creator in Nodejs

`npm i exceljs ` [more](https://www.npmjs.com/package/exceljs)

```javascript
const ExcelJS = require('exceljs');

 const workbook = new ExcelJS.Workbook();
        const worksheet  = workbook.addWorksheet("Hisobot");
        worksheet .addRow(['First column title', 'Second column title']);



 worksheet .addRow(["First column value", "Second column value"]);


const filePath = 'fileName.xlsx';
        workbook.xlsx.writeFile(filePath)
            .then(()=> {
                console.log('Excel file created successfully.');
            })
            .catch(function(error) {
                console.error('Error:', error);
            });

```
