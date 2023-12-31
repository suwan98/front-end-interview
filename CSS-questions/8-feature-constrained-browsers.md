# Q : 기능이 제한된 브라우저에 페이지를 제공하는 방식은 무엇인가요? 어떤 기술이나 과정을 사용하나요?

<br />

# A : 기능이 제한된 브라우저에 웹페이지를 제공하는 방식은 주로 '점진적 향상'과 '우아한 퇴보'라는 두가지 전략을 사용합니다.

**두가지 전략은 모두 웹 접근성과 호환성을 높이기 위해 사용됩니다**

1. 점진적 향상 (Progressive Enhancement)

- 기본적인 `HTML` 마크업을 작성해 최소한의 기능을 제공합니다.
- `CSS`를 추가해 레이아웃과 스타일을 개선합니다.
- `JavaScript`를 추가해, 상호작용성을 향상하거나, 추가기능을 제공합니다.
- 이러한 과정은 모든 사용자가 기본적인 내용과 기능에 접근할 수 있도록 하며, 브라우저의 기능이나 네트워크 조건에 따라 사용자 경험을 점진적으로 향상시키는것을 목표로 합니다.

2. 우아한 퇴보 (Graceful Degradation)

- 최우선적으로 최신 기능이 포함된 완전한 사용자 경험을 구축합니다.
- 이후 브라우저나 기기가 최신 기능에 지원하지 않을 때를 대비해, 기본 기능과 내용이 여전히 사용자에게 제공될 수 있도록 구성합니다.
- 우아한 퇴보 방식은 새로운 기술을 최대한 활용하면서도, 더 오래된 기술을 사용하는 사용자들도 여전히 콘텐츠를 접근할 수 있도록 하는 방식입니다.

**위 두가지 전략을 구현할 때 사용하는 기술과 과정은 다음과 같습니다**

- 여러 콘텐츠들의 가용성을 보장하기 위해 `HTML`을 시맨틱하게 작성합니다.
- `CSS`에서는 `@media` 쿼리를 사용해 다양한 화면 크기와 해상도에 대응하는 반응형 웹을 구성합니다.
- 자바스크립트의 기능탐지를 사용해, 브라우저가 특정 `API`나 기능을 지원하는지 확인하고, 지원하지 않을 경우 대체기능을 제공할 수 있도록 합니다.
- 폴리필을 사용해 최신 웹 `API`가 없는 브라우저에서도 해당 기능을 사용할 수 있도록 구성합니다.
- 접근성을 고려해 `WAI-ARIA` 구성, 스크린 리더 최적화를 수행합니다.
