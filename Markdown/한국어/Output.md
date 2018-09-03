Output
===
Output 속성은 어디에, 어떻게 번들된 파일을 내보낼지에 대한 내용을 담고 있습니다. Output은 다음과 같이 사용합니다.
```javascript
const path = require('path');

module.exports = {
  entry: './src/index.js',
  // output.filename = name of bundle, output.path = where it to be emitted.
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js'
  }
};
```