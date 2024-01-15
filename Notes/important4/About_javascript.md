## Javascript 
싱글 스레드이면서 논 블로킹 언어이다.

### 싱글스레드 
* 스레드가 하나 밖에 존재하지 않아 한번에 하나의 작업만 할 수 있다.

### 논블로킹
* 하나의 요청이 완료될 때까지 기다리지 않고 동시에 다른 작업을 수행함

### 동기적 비동기적 
* 일반적으로 자바스크립트는 동기적인 언어이다.
* 하지만, setTimoout, 이벤트리스너, ajax 함수를 사용하면 비동기 처리 가능
  [비동기적 처리]
* 이벤트 발생 시, 호출할 콜백함수를 관리하고 실행 순서를 결정한다.
  (콜백함수? 특정 코드가 마무리 되기 전에 실행되지 않도록 하는 함수)
  [콜백함수의 단점]
  * 콜백지옥: 비동기 처리를 중첩시켜서 코드를 작성하기 때문에, 예외처리가 어렵고 복잡도 증가
    => 해결하기 위해 Promise가 나옴

* web API(대기실)에 이벤트를 보내놓고 실행 순서에 따라 Callback Queue에 집어 넣은 다음, Call stack이 비었을 때 Event loop를 사용하여 차례대로 스택으로 밀어넣는다.
* Callback Queue에는 엄밀히 말하면 2가지 큐가 있고, 우선순위가 높은 마이크로 테스크 큐가 먼저 stack에 올려진다.(= 우선순위 큐)
  * 마이크로태스크 큐(microtask queue) vs 테스크 큐(Task queue)
    1. microtask queue 👉 Promise
    2. task queue, macrotask queue 👉 setTimeout, setInterval
      

### 콜백지옥 해결
1. Promise
* 콜백 지옥을 해결하는 방법 중 하나로 ES6에서 지원
* 비동기에서 성공과 실패를 분리해서 메소드를 수행
[생성]
* `new Promise`
* 함수의 값 true면 resolve() 실행 : fullfilled
* 에러가 나면 reject() 실행

2. async & await
* 비동기 처리 패턴 중 가장 최근에 나온 문법
* 위에서부터 아래로 차근차근 사고해나갈 수 있도록 간결하게 짜여진 읽기 좋은 코드
* async: 항상 Promise 반환
* await: promise가 처리될 때까지 기다린다.
