# Q : debounce에 대해서 설명해주세요.

<br />

# A : Debounce란 일정 시간동안 연속적으로 발생한 이벤트들 중에 마지막 하나만 실행시켜 과다한 호출이나 렌더링을 막는 최적화 기술입니다.

- 프로젝트에서 회원가입 기능 구현시, ID값을 입력 시 실시간 Validation 중 onChange 이벤트가 과도히 호출되어 해당 함수를 debounce 유틸리티 함수로 매핑해 지정된 시간에서의 마지막 입력값만을 받도록 적용한 경험이 있었습니다.

### Debounce 구현 코드는 다음과 같습니다.

- 설정한 delay 시간 내 함수가 재실행된다면 내부 클로저 함수에 의해 clearTimout 되므로 제거되고, 시간내 아무런 호출이 없다면 가장 마지막으로 호출된 setTimeout 내부 함수가 실행되게 됩니다.

```ts
const debounce = <T extends (...args: any[]) => any>(fn: T, delay: number) => {
  let timeout: ReturnType<typeof setTimeout>;

  return (...args: Parameters<T>): ReturnType<T> => {
    let result: any;
    if (timeout) clearTimeout(timeout);
    timeout = setTimeout(() => {
      result = fn(...args);
    }, delay);
    return result;
  };
};
```
