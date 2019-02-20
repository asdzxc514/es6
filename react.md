## 0\. 강좌
https://velopert.com/reactjs-tutorials

## 1\. React?

React는 페이스북에서 개발한 유저인터페이스 라이브러리로서 개발자로 하여금 재사용 가능한 UI를 생성 할 수 있게 해줍니다.&nbsp;이 라이브러리는 현재 페이스북, 인스타그램, 야후, 넷플릭스를 포함한 많은 큰 서비스에서 사용되고 있습니다.

이 라이브러리는**&nbsp;Virtual DOM** 이라는 개념을 사용하여 상태의 변함에 따라 선택적으로 유저인터페이스를 렌더링합니다.
따라서, 최소한의 DOM 처리로 컴포넌트들을 업데이트 할 수 있게 해줍니다.

## 1-2\. React-native
모바일 웹을 만들도록 도와주는 library

## 2\. Virtual DOM은 어떻게 작동하지?

> 데이터가 업데이트되면, 전체 UI 를 Virtual DOM 에 리렌더링 합니다.  
> 이전 Virtual DOM 에 있던 내용과 현재의 내용을 비교합니다.  
> 바뀐 부분만 실제 DOM 에 적용이 됩니다.  

무조건 위의 3가지가 처리 되는것이 아니라 개발하는것에 따라 무조건 전체 렌더링 할 수도 있음  
실제 DOM을 처리하는 건 비용이 많이 들고 느림  
처리해야할 데이터가 많아지면 더 많은 부담이 되는 것을 줄여줌  

## 3\. 특징

*   **JSX** - JSX는 JavaScript의 Syntax 확장입니다. JSX를 사용하는것이 필수는 아니지만, 사용하는것이 권장됩니다.
*   **Components** - React는 전부 Component에 대한 것 입니다. React 개발을 할땐 모든것을 Component로서 생각해야 합니다.
*   **단일방향 (Unidirectional) 데이터 흐름 & Flux** - React에선 데이터가 단일방향으로만 흐릅니다. 데이터 흐름을 단방향으로 제한함으로서 데이터를 추적하기 쉽고 디버깅을 쉽게 해줍니다. Flux는 데이터가 단일방향으로 흐르는것을 유지해주는 패턴입니다. ( Flux에 대해선 나중에 자세히 알아보겠습니다. )

## 4\. 장점

*   React는 JavaScript 객체 형태의 Virtual DOM 을 사용하여 어플리케이션의 성능을 향상시킴 (JavaScript Virtual DOM 처리가 실제 DOM 보다 빠르기 때문)
*   서버 & 클라이언트 사이드 렌더링 지원을 통해 브라우저측의 초기 렌더링 딜레이를 줄이고, SEO 호환도 가능해짐
*   Component 의 가독성이 매우 높고 간단하여 쉬운 유지보수, 간편한 UI 수정 및 재사용 용이
*   React는 프레임워크가 아닌 라이브러리기 때문에 다른 프레임워크와 혼용 가능

## 5\. 단점
*   VIEW ONLY , VIEW 이외의 기능은 써드파티 라이브러리(Third party library, =패키지, 모듈로 불리기도함)를 이용하거나 직접 구현해야함
*   IE8 이하 지원하지 않음 (IE8 이하 버전을 지원해야 할 경우 v0.14 버전을 사용 해야함)
*   React는 inline-template 과 JSX 를 사용하는데, 일부 개발자들에게는 적응이 안 될 수 있음

## 7\. Babel
2015년에 업데이된 ES6를 사용할 때, 이전 문법인 ES5로 변환해주는 Preprocessor  
최신버전의 크롬이나 파이어폭스는 지원하지만, 구 버전의 브라우저나 IE를 위해 변환함

## Hello World
```js
import React from 'react';    // var React = require('react');  와 동일

function HelloWorld (props) {
  return (
    <h1>Hello {props.name}!</h1>
  );
}

export default HelloWorld;
```
 webpack 이라는 도구를 사용하여 마치 Node.js 에서 require 하는것과 같이 모듈을 불러올 수 있게 하는 것!


## 용어정리

`번들링(bundling)` : webpack 은 이렇게 import(혹은 require) 한 모듈들을 불러와서 한 파일로 합치는 작업  
`프롭스(props)` : 변수