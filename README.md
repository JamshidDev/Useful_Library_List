# Useful_Library_List
My best used libraries and usage guides











#  1.[SheetJS](https://sheetjs.com/)

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


#  3.[ExcelJS](https://github.com/exceljs/exceljs#readme)

> Excel file reader in Nodejs

`npm i exceljs ` [more](https://www.npmjs.com/package/exceljs)

```javascript
const ExcelJS = require('exceljs');

 const workbook = new ExcelJS.Workbook();
        const worksheet  = workbook.addWorksheet("Hisobot");
        worksheet .addRow(['Vagon raqami', 'Chiqqan stansiya', 'Turgan stansiya', "Borayotgan stansiya", "Index"]);

 const rowNumber = 1;

        // Fill color you want to set
        const fillColor = {
            type: 'pattern',
            pattern: 'solid',
            fgColor: { argb: '85b2f9' } // Red background color
        };

 worksheet.getRow(rowNumber).eachCell({ includeEmpty: true }, cell => {
            cell.fill = fillColor;
        });

 worksheet .addRow([station.vagon_number, station.first_station.station_name_ru, station.current_station.station_name_ru, station.last_station.station_name_ru, station.index,]);
const filePath = './download/nodenReports.xlsx';
        workbook.xlsx.writeFile(filePath)
            .then(()=> {
                console.log('Excel file created successfully.');
                let file_path =  new InputFile(filePath)
                ctx.replyWithDocument(file_path)
            })
            .catch(function(error) {
                console.error('Error:', error);
            });

```
