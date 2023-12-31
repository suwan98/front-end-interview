# Q : CSS `<link>`는 `<head></head>` 사이에, JS `<script>`는 `</body>` 직전에 위치시키는 것이 일반적으로 좋은 아이디어인 이유는 무엇인가요? 예외 상황은 알고 있나요?

<br />

# A :

**CSS `Link` 태그를 HTML의 `Head` 내부에 위치시키는 이유는 웹 페이지가 로딩 될때 먼저 스타일이 우선적으로 적용되어야하기 때문입니다.**

- 웹페이지가 로딩되는 동안 스타일이 적용되지 않는다면, 사용자는 스타일이 적용되지 않은 콘텐츠를 보게되는데,
- 이를 FOUC(Flash of Unstyled Content)라고 합니다
- 이러한 현상은 사용자 경험에 좋지않은 영향을 끼칠 수 있게됩니다.

**반면에 JavaScript의 `<script>` 태그는 `</body>` 직전에 위치시키는것이 좋은이유는**

- `JavaScript` 파일이 로딩과 실행이 페이지의 렌더링을 차단하기 때문입니다
- `<script>` 태그를 `<head>` 부분에 위치시킨다면 웹 브라우저는 스크립트를 완전히 로딩하고 실행할 때까지 웹 페이지 렌더링을 중단시키게 됩니다.
- 결과적으로 사용자는 빈화면을 보게될것이고 이또한 사용자경험에 좋지않은 영향을 미칩니다.
- 따라서 보통 `script` 태그는 페이지의 렌더링이 중단되지 않도록 `<body/>` 직전에 위치 시키는것이 일반적입니다.

**그러나 예외사항도 존재합니다**

- 스크립트가 문서의 나머지 부분에 의존하지않고 페이지 로딩 시 초기데이터를 설정하거나 다른스크립트를 로드하는 경우
- `HTML`의 `<head>` 부분에 위치하는 방법이 더욱 많이 사용됩니다.
- 이에 `<head>` 부분에 스크립트를 위치할 시엔 `async`나 `defer` 속성을 통해 스크립트가 `HTML`문서에 의존하지 않도록 비동기적으로 설정해야합니다.
- 그리고 `CSS`도 일반적으로 `<head>` 부분에 위치하지만 경우에 따라서 `JavaScript`와 마찬가지로 렌더링 차단을 유발할 수 있습니다
  - 예를 들어, 용량이 큰 `CSS`파일을 로드해야 할 시 해당 `CSS` 파일을 `HTML`의 `<body/>` 직전에 위치시키고 `media` 속성을 사용해 렌더링 차단을 방지할 수 있게 됩니다
