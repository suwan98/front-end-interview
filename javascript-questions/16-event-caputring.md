# Q : 이벤트 캡처링에 대해 설명해주실 수 있을까요?

<br />

# A : 이벤트 캡쳐링이란 이벤트 버블링과 반대로 최상위 태그에서 해당 태그가 전파되는 과정입니다.

- 구현방법으론 할당한 핸들러의 3번째 옵션으로 `{capture : true}`를 설정합니다.