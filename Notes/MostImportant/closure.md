## 클로저(Closuer)
* 클로저는 함수와 그 함수가 선언된 렉시컬 환경의 조합이다.
  ( 함수 내에 함수가 선언될 경우, 중첩된 함수에서 외부 변수를 읽을 수 있다.)
* 함수가 자신의 외부 변수에 접근할 수 있다는 것을 의미한다.
* 장점
  1. 데이터 은닉: 함수 내부의 변수를 외부에서 접근하지 못하도록 숨길 수 있다.
  2. 비동기 처리

```
function counter() {
  let count = 0;
  function inner() {
    count++;
    console.log(count);
  }
  return inner;
}

const increment = counter();
increment(); // 1
```
