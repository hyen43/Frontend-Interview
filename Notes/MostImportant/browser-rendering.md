##브라우저 렌더링 과정

1. HTML을 파싱 후, DOM 트리를 구축한다.
2. CSS 파싱 후, 스타일 규칙(CSSOM)을 구축한다.
3. Javascript를 실행한다.
4. DOM 트리와 스타일 규칙이 결합하여, 렌더트리를 구축한다.
5. 뷰포트 기반으로 렌더트리의 각 노드가 가지는 정확한 위치와 크기를 계산한다.(layout단계)
6. 계산한 위치/크기를 기반으로 화면에 그린다.(paint단계)

[그림]
![image](https://github.com/hyen43/Frontend-Interview/assets/60104321/cdfc4035-432e-4f0a-98ee-e8a0b4488143)

* 참고문헌: https://d2.naver.com/helloworld/59361
