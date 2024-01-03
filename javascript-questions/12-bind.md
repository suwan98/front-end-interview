# Q : Function.prototype.bind에 대해 설명해주실 있을까요?

<br />

# A : bind 함수는 함수가 가리키는 `this`만 조작하며 `call/apply`와 달리 호출은 하지않는 것입니다.

- 즉 정의하고자하는 새로운 `this`를 정의한 후 그 함수를 복사해 새로운 함수를 만들어 리턴하는것과 같습니다.
