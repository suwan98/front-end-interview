# Q : `doctype`은 어떤 기능을 하나요?

<br />

# A :

- `HTML`에서 `doctype`은 모든 문서의 최상단에 있는 필수로 들어가야하는 서문입니다.
- `doctpye` 선언은 `HTML` 문서가 어떤 버전으로 작성되었는지 브라우저에게 알려주는 역할을 합니다.
- 이렇게 선언하는 이유는 호환성을 높이기 위해서인데, `HTML`은 버전마다 적용되는 태그와 적용되지 않는 태그가 나뉜다.
- 구버전에서 신버전의 `HTML` 태그를 사용을 하게된다면, 웹 브라우저에서 문법오류로 간주하는데, 해당 선언을 통해 구버전과 신버전에 알맞게 문법 검사를 하는 역할을 수행하게 된다.

```html
<!DOCTYPE html>
```
