Loaders
===
webpack은 JavaScript 파일들 밖에 이해하지 못합니다. Loaders는 다른 유형의 파일들도 변환하여 의존성 그래프에 추가할 수 있는 유효한 모듈로 만듭니다. 예를 들어서 `.css` 파일과 같은 파일을 의미합니다. Loaders는 다음과 같이 사용합니다.
```javascript
const path = require('path');

module.exports = {
  output: {
    filename: 'bundle.js'
  },
  module: {
    rules: [
      // test property = file or files that should be transformed
      // use property = which loader should be use
      { test: /\.txt$/, use: 'raw-loader' }
    ]
  }
}
```
`test` 속성은 해석되어야하는 파일 또는 파일들을 나타냅니다. 정규표현식을 사용하여 파일의 확장자명을 작성하는 형태로 적습니다. `use` 속성은 `test` 에 명시된 파일을 읽는데 사용될 loader를 적습니다. 위의 예제는 .txt 파일을 읽기 위해서 raw-loader를 사용한다는 의미를 담고 있습니다.