# capture-action

[中文文档](./README_zh.md)   [document](./README.md)

capture user action in browser
- [install](#install)
- [usage](#usage)
  * [API quick run](#api-quick-run)
- [develop](#develop)
  * [file structure](#file-structure)
  * [run tests](#run-tests)
- [license](#license)

## install

`npm i capture-action --save` or `npm i capture-action --save-dev`

Install on global, using `npm i capture-action -g`



## usage








### API quick run



```js
let capturer = require('capture-action')
let capture = capturer({
 eventListType: ['click', 'keydown'],
 onlyUserAction: false // set true will ignore none-user action
});

let {start, stop} = capture((action, event) => {
    // handle action and event here!
});

start(); // start to capture user action

stop(); // stop to capture user action

start(); // resume
```




## develop

### file structure

```
.    
│──LICENSE    
│──README.md    
│──README_zh.md    
│──debug    
│   │──test0    
│   │   │──assets    
│   │   │   └──app.js    
│   │   │──index.html    
│   │   │──index.js    
│   │   └──webpack.config.js    
│   └──testInputNumber    
│       │──assets    
│       │   └──app.js    
│       │──index.html    
│       │──index.js    
│       └──webpack.config.js    
│──index.js    
│──package.json    
│──src    
│   │──captureEvent.js    
│   │──index.js    
│   └──nodeUnique.js    
└──test    
    │──browser    
    │   │──base.js    
    │   │──fixture    
    │   │──resume.js    
    │   └──stop.js    
    └──function    
        └──index.js     
```


### run tests

`npm test`

## license

The MIT License (MIT)

Copyright (c) 2016 chenjunyu

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
