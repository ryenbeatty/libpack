### Test library package with Webpack

```
npm install git+https://github.com/UsulPro/libpack.git --save
```

```
// index.js:

const fs = require('fs');
const logo =  require('libpack').logo;
const style =  require('libpack').style;

const htmlData = `
<div>
  <style>
    ${style()}
  </style>
  <img src="${logo()}" alt="logo" title="logo" width="200px"/>
</div>
`;

fs.writeFile('test.htm', htmlData, (err) => {
  if (err) throw err;
  console.log('It\'s saved!');
});
```

```
$ node .
```

open `test.htm` in your browser