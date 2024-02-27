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


#  3.[docxtemplater](https://github.com/open-xml-templating/docxtemplater#readme)

> DOCX file creator in Nodejs

`npm install --save docxtemplater pizzip ` [more](https://www.npmjs.com/package/docxtemplater)

```javascript
const Docxtemplater = require('docxtemplater');
const PizZip = require("pizzip");
const path = require("path");

 const content = fs.readFileSync(
            path.resolve(__dirname, "template.docx"),
            "binary"
        );
        const zip = new PizZip(content);

        const doc = new Docxtemplater(zip, {
            paragraphLoop: true,
            linebreaks: true,
        });
        doc.render({
            variable1: "Variable one",
            variable2: "Variable two",
        });

 const buf = doc.getZip().generate({
            type: "nodebuffer",
            compression: "DEFLATE",
        });


        fs.writeFileSync(path.resolve(__dirname, "output.docx"), buf);
```


#  4.[moment-timezone](https://momentjs.com/timezone/)

> Parse and display dates in any timezone.

`npm i moment-timezone ` [more](https://www.npmjs.com/package/moment-timezone)

```javascript
const moment = require('moment-timezone');

// Set the timezone
const timezone = 'America/New_York';

// Get the current time in the specified timezone
const currentTimeInNY = moment.tz(timezone);

// Display the current time in New York
console.log('Current time in New York:', currentTimeInNY.format());

// Convert a specific time to New York timezone
const specificTime = '2024-02-27T12:00:00';
const specificTimeInNY = moment.tz(specificTime, timezone);

// Display the specific time in New York
console.log('Specific time in New York:', specificTimeInNY.format());

// Convert a specific time from one timezone to another
const timeInLosAngeles = '2024-02-27T12:00:00';
const timeInLA = moment.tz(timeInLosAngeles, 'America/Los_Angeles');

// Convert to New York timezone
const timeInNY = timeInLA.clone().tz('America/New_York');

// Display the converted time in New York
console.log('Converted time in New York:', timeInNY.format());
```

