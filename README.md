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
_ex)  function(value)  {  return value }    ===   (value) => { return value }_  
  
  
  
## 코드설명 

1. const 로 선언된 array 는 (...elements) 인자를 받아서 elements 를 리턴합니다.  
...elements 에서 앞에 붙은 ... 은 인자를 강제적으로 배열로 받는 다는 뜻 입니다.  
2. array(1, 2, 3)  으로  array 함수를 실행 했다면  결과값은 배열로 변경되어 [1, 2, 3] 이 됩니다.  
3. 마찬가지로 const 로 선언된 log 는 ...args 를 인자로 받게됩니다.  
4. log 함수를 실행하면 'hello' , 'Seoul' 이 배열로 변경되어 출력되는 것을 확인 할 수 있습니다.    


## THIS
  
1. Global Scope에서 사용될 때 this는 전역 객체를 가르킨다(window 객체)  
2. 함수에서 사용될 때에도 this는 전역 객체를 가르킨다.(window 객체)  
3. 객체에 속한 메서드에서 사용될 때 this는 메서드가 속한 객체를 가르킨다.  
4. 객체에 속한 메서드의 내부함수에서 사용될 때 this는 전역 객체를 가르킨다.(window 객체)  
5. 생성자에서 사용될 때, this는 이 생성자로 인해 생성된 새로운 객체를 가르킨다.  
  
이렇게 정리해놓고 보니, 4번의 경우를 제외하고 this도 일반적으로 자기가 속한 객체를 가르키는것으로 알 수 있다.  