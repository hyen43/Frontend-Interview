## 호이스팅
변수 및 함수 선언문이 스코프 내에서 최상단으로 끌어올려지는 현상을 말한다. (= 최상단에서 선언된다.)

### 호이스팅 대상
* var 변수 선언
  (단, var 변수가 할당되면 끌어올려지지 않는다.) 
* 함수선언문 O (함수표현식 x)
```
foo(); // "함수선언문"
foo2(); // ERROR 

function foo() {
  console.log("함수선언문");
}

function foo2() {
  console.log("함수표현식");
}
```

### 참고자료 
https://gmlwjd9405.github.io/2019/04/22/javascript-hoisting.html
