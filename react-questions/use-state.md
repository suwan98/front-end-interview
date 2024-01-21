# Q : useState에 대해서 설명해주세요

<br />

# A : useState는 함수형 컴포넌트에서 상태를 관리할 수 있게 하는 Hook입니다.

**useState는 하나의 인자를 받습니다. 이 인자는 상태의 초기값을 설정하는데 사용됩니다.**

- useState는 배열을 리턴하는데 첫번째 값은 현재상태를 나타내는 state, 두번째 값은 상태를 갱신해주는 setState 함수입니다.
  - setState를 호출하면 호출된 setState 함수의 인자에 의해 상태가 업데이트됩니다.
  - 이에 따라 최종적으로 setState에 의해 갱신된 최신 상태 값을 가진 컴포넌트가 리렌더링됩니다.

```js
const [state, setState] = useState(0);
```
