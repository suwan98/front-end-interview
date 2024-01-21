# Q : useRef에 대해서 설명해주세요.

<br />

# A : 리액트로 개발 시 Vanlia JavaScript의 document.querySelecotor와 같이 특정 DOM을 직접 선택해야하는 상황이 발생할 수 있습니다. 이런 경우에 useRef를 사용합니다.

**useRef Hook을 통해 특정 DOM Node에 접근하고 참조할 수 있게됩니다.**

- useRef의 매개변수로는 직접 선택하고자 하는 DOM Node의 초깃값입니다.
- useRef를 통해 ref 객체를 만들고, 해당 객체를 선택하고자 하는 DOM에 ref의 값으로 설정해야합니다.
- 이를 통해 ref 객체의 current 프로퍼티의 값은 선택한 DOM을 가르키게 됩니다.
- useRef는 useState와 달리 리렌더링을 일으키지않으며, 특정 정보를 기억하고 싶을 경우에 사용됩니다.
