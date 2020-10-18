# A JavaScript Library For Printing – Print.js

## Description:
Print.js is a small yet powerful JavaScript library which enables you to preview and print any elements (PDF, HTML, IMAGE, DYNAMIC DATA) on the webpage.


## Installation:

###### To install using npm:
```npm install print-js --save```

###### To install using yarn:
```yarn add print-js```

###### When installing via npm or yarn, import the library into your project:
```import print from 'print-js'```



## How to use it:

Include both print.css and print.js on the webpage.
  ```html
  <script src="print.js"></script>
<link rel="stylesheet" href="print.css">
```

Print a PDF file on the webpage without opening or downloading.
  ```javascript
  printJS('sample.pdf')
  ```
  
Print HTML content.
  ```javascript
  printJS('SELECTOR', 'html')
  ```
  
Print an image on the webpage.
  ```javascript
  printJS('img.jpg', 'image');
  ```
  
Print dynamic data (e.g. JSON) on the webpage.
  ```
  mydata = [
    {
       name: 'John Doe',
       email: 'john@doe.com',
       phone: '111-111-1111'
    },
    {
       name: 'Barry Allen',
       email: 'barry@flash.com',
       phone: '222-222-2222'
    },
    {
       name: 'Cool Dude',
       email: 'cool@dude.com',
       phone: '333-333-3333'
    }
 ];

 printJS({
   printable: mydata, 
   properties: ['name', 'email', 'phone'], 
   type: 'json'
})
```


All default parameters.
  
  ```javascript
  // Document source: pdf or image url, html element id or json data object.
printable: null,

fallbackPrintable: null,

// Document type.
type: 'pdf',

// Optional header to be used with HTML, Image or JSON printing. 
// It will be placed on the top of the page.
header: null,

// Max document width in pixels. 
maxWidth: 800,

// Font Family
font: 'TimesNewRoman',

// Font size
font_size: '12pt',

// Used to keep or remove padding and margin from elements that are being printed.
honorMarginPadding: true,

// Print text in color
honorColor: false,

// Used when printing JSON.
properties: null,

// grid header when printing JSON data
gridHeaderStyle: 'font-weight: bold; padding: 5px; border: 1px solid #dddddd;',

// grid rows when printing JSON data
gridStyle: 'border: 1px solid lightgray; margin-bottom: -1px;',

// Enable this option to show user feedback when retrieving or processing large PDF files.
showModal: false,

// Message displayed to users when showModal is set to true.
modalMessage: 'Retrieving Document...',

// Frame ID
frameId: 'printJS',

// Document title
documentTitle: 'Document',

// Target styles
targetStyle: ['clear', 'display', 'width', 'min-width', 'height', 'min-height', 'max-height'],
targetStyles: ['border', 'box', 'break', 'text-decoration'],

// Elements to ignore
ignoreElements: [],

// Image style
imageStyle: 'width:100%;',

// Repeat table header
repeatTableHeader: true,

// Pass one or more css files URLs
css: null,

// Pass a string with custom style
style: null,

// When set to false, the library will not process styles applied to the html being printed. Useful when using the css parameter.
scanStyles: true,

// Callback functions
onLoadingStart: null,
onLoadingEnd: null,
onPrintDialogClose: null,
```

## Links
https://printjs.crabbly.com/
  




  
