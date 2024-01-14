# Q : ES6 클래스와 ES5 함수 생성자의 차이는 무엇인가요?

<br />

# A : 둘다 인스턴스를 생성하는 생성자 역할을 하지만 상속을 구현하는 방법에 있어서 차이점이 존재합니다.

````js
// ES5 Function Constructor
function Person(name) {
  this.name = name;
}
// ES6 Class
class Person {
  constructor(name) {
    this.name = name;
  }
}```
````

- `ES5`에서는 생성자 함수를 상속받기 위해 `prototype`에 새로운 객체를 복사하는 등 여러가지 작업이 필요합니다.
- 그러나 클래스는 `extends`키워드를 통해 상속받을 클래스를 명시하고, `constructor` 메서드에서 `super` 키워드를 통해 자식클래스에서 부모 클래스의 값을 가져 사용할 수 있게됩니다.
