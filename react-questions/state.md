# Q : React에서 State의 불변성을 유지해야하는 이유를 설명해주세요.

<br />

# A : React에서 상태의 불변성을 지키지 않으면 상태의 값이 새로이 업데이트되어도 바뀐 값을 감지하지 못하게 됩니다.

**그 이유는 리액트에서 이전상태와 새로운 상태를 비교할때 두 상태가 같은 객체를 참조하고 있다고 판단되면 리액트는 상태가 변경되지 않았다고 판단하기 때문입니다.**

- 이는 JavaScript에서 객체나 배열과 같은 참조타입은 내용이 변경되어도 참조 값이 변하지 않는 특성과 일치합니다.
- 따라서 상태를 직접적으로 수정하는 대신 해당 상태를 복사하여 복사한 상태를 업데이트해야합니다.
- 이를 기반으로 리액트는 새로운 참조값과 이전 참조값을 비교하여 상태가 업데이트 되었음을 확인하고 이를 기반으로 리렌더링을 진행할 수 있게됩니다.
