# Q : var person = Person(), var person = new Person()의 차이는 무엇인가요?

<br />

# A : 둘의 차이점은 일반함수로 호출하는것이냐, 생성자함수로써 함수를 호출하것이냐의 차이입니다.

**`var person = Person()`는 `Person`이라는 함수를 일반함수로서 호출하는것인데,**

- 이때 `this`는 `Person` 함수 내부에선 웹브라우저에선 전역 객체인 `window`를 가리키게 됩니다.

**`var person = new Person()`은 `Person`을 생성자 함수로서 호출하고, 새로운 인스턴스를 생성하는것입니다.**

- 이때 `this`는 새로이 생성된 객체를 바인딩합니다.
- 그래서 `new` 키워드를 사용하면 `Person`의 인스턴스가 생성되고, 그 인스턴스는 `Person` 생성자 함수의 프로포타입을 상속받게 됩니다.
