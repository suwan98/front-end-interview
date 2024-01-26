# Q : useState를 Vanlia JavaScript로 간단히 구현한다면?

<br />

# A : useState를 구현한다면 다음과 같습니다.

**useState는 다음과 같은 특징이 존재합니다**

1. 상태는 초기화 이후 setState를 통해서만 변경이 가능합니다.
2. setState에 의해 값이 변경되면 해당하는 컴포넌트는 자동으로 리렌더링이 발생합니다.

```js
let _state = [];
let _index = 0;

function useState(initState, component, $target) {
  const index = _index++;
  const state = _state[index] || initState;

  const setState = (newState) => {
    _state[index] = newState;
    _index = 0;
    component($target);
  };

  return [state, setState];
}
```
