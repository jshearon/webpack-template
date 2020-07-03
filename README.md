# Webpack Template

## Setup Checklist
1. - [ ] Initialize as a webpack project
```js
npm init -y
```

2. - [ ] Edit package.json
```json
  "main": "src/javascripts/main.js",
```
```json
  "scripts": {  
    "start": "webpack-dev-server --mode development --open",
    "build": "webpack --mode production --module-bind js=babel-loader",
    "deploy": "npm run build && firebase deploy"
  },
  ```
```json
  "author": "Jonathan Shearon",
  "license": "MIT"
}
```


3. - [ ] Install Dev Dependencies
```sh
npm install @babel/core @babel/preset-env babel-loader css-loader eslint eslint-config-airbnb-base eslint-loader eslint-plugin-import file-loader html-loader html-webpack-plugin mini-css-extract-plugin node-sass sass-loader webpack webpack-cli webpack-dev-server --save-dev
```


4. - [ ] Install Front End Dependencies
```sh
npm install axios bootstrap firebase jquery popper.js @fortawesome/fontawesome-free --save
```

## Optional

### Including Images
```js
import cat from './assets/cat.jpg';

let domString = `<img src=${cat} alt="picture of a cat"/>`;

document.getElementById('cat').innerHTMl = domString;
```

### Axios

#### Using Axios
> For every file you will need to make an XHR request in, you will need to require Axios
```js
import axios from 'axios';

const examplePromise = () => new Promise((resolve, reject) => {
  axios.get('http://localhost:3001/example')
    .then((data) => {
      resolve(data);
    })
    .catch((error) => {
      reject(error);
    });
});
```
