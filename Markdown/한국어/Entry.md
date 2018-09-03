Entry
===
Entry 포인트는 Webpack이 내부 종속성 그래프를 도출하기 위해서 사용해야하는 모듈을 나타냅니다. 간단히 설명하자면, 내부 종속성 그래프의 루트 노드, 즉, 번들링의 시작점을 나타냅니다. Entry 포인트는 다음과 같이 나타냅니다.
```javascript
module.exports = {
  // key = entry, value = start file path
  entry: './src/index.js'
};
```