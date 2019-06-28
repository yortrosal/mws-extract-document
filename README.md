# mws-base64-zip
[Work around](https://docs.developer.amazonservices.com/en_US/fba_inbound/FBAInbound_ExtractingPdfDocumentData.html) to extract Zip/PDF Document from MWS Base64-encoded string mws api response.

## MWS End-Points
 - GetPackageLabels
 - GetUniquePackageLabels
 - GetPalletLabels
 - GetBillOfLading

## Install
```
$ npm install mws-base64-to-zip --save
```

## Basic Usage

```js
const mwsBase64ToZip = require('mws-base64-to-zip');

const dist = './folder/to/document.zip';
const base64String = ''; //located at PdfDocument data response from MWS api.

// PROMISE
mwsBase64ToZip(base64String, dist)
  .then((msg)=>{
    // file saved. do something here...
    console.log(msg);
  })
  .catch(err)=>{
    console.log(err);
  });
```

## License
MIT © [Jorge Rosal](https://github.com/yortrosal)
