# Useful_Library_List
My best used libraries and usage guides











#  [SheetJS](https://sheetjs.com/)

> The SheetJS Community Edition offers battle-tested open-source solutions for extracting useful data from almost any complex spreadsheet and generating new spreadsheets that will work with legacy and modern software alike.

`npm i xlsx `

```javascript
function test(){
	console.log("Hello world!");
}
 
(function(){
    var box = function(){
        return box.fn.init();
    };

    box.prototype = box.fn = {
        init : function(){
            console.log('box.init()');

			return this;
        },

		add : function(str){
			alert("add", str);

			return this;
		},

		remove : function(str){
			alert("remove", str);

			return this;
		}
    };
    
    box.fn.init.prototype = box.fn;
    
    window.box =box;
})();

var testBox = box();
testBox.add("jQuery").remove("jQuery");
```
