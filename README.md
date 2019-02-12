# ES6

`Babel` ES6코드를 ES5로 변환하는 transpiler다  
`const` ES6 의 새로운 문법으로 const 로 선언된 값은 외부에서 직접적으로 변경할 수 없습니다.    
  
  
```
const array = (...elements) => { 
    return elements; 
}; 

array(1,2,3);    // [1, 2, 3] 

const log = (...args) => { 
    console.log(...args); 
} 

log('hello', 'Seoul');    // hello Seoul
```


`arrow function :  ( ) => { }` 로 실행하며 ( ) 의 값은 인자로 받고, { } 은 함수의 실행구문을 넣습니다.  
###### ex)  function(value)  {  return value }    ===   (value) => { return value }    
  
  
  
## 코드설명 

1. const 로 선언된 array 는 (...elements) 인자를 받아서 elements 를 리턴합니다.  
...elements 에서 앞에 붙은 ... 은 인자를 강제적으로 배열로 받는 다는 뜻 입니다.  
2. array(1, 2, 3)  으로  array 함수를 실행 했다면  결과값은 배열로 변경되어 [1, 2, 3] 이 됩니다.  
3. 마찬가지로 const 로 선언된 log 는 ...args 를 인자로 받게됩니다.  
4. log 함수를 실행하면 'hello' , 'Seoul' 이 배열로 변경되어 출력되는 것을 확인 할 수 있습니다.    
