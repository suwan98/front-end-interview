# Q : 효율적인 CSS를 작성하기 위한 "주의점"은 무엇인가요?

<br />

# A : 효율적인 CSS를 작성하기 위한 주의점은 다음과 같습니다.

**1. 선택자의 특이성(Specificity) 관리하기**

- 너무 구체적인 선택자는 재사용성을 떨어뜨립니다.
  - 따라서 유지보수가 어려워질 수 있으므로, 가급적으로 클래스 기반 선택자를 사용하는 것이 좋습니다.
- `ID` 선택자와 태그 선택자의 사용을 최소화 할 수 있도록 합니다.

**2. 중복 코드 최소화하기**

- 웹 내에서 중복적으로 사용되는 공통 스타일은 재사용할 수 있도록 클래스를 만들어 사용합니다.
- `CSS` 프로세서 `Sass`등을 활용해, 스타일 변수, 믹스인, 함수등을 만들어 중복을 최소화 할 수 있습니다.

**3. 캐스케이딩과 상속 이해하기**

- 가능한 상속을 활용해, 부모 요소에서 자식 요소로 공통된 스타일을 전달합니다.

**4. 미디어 쿼리의 효율적 사용하기**

- 반응형 디자인 구현을 위해 미디워 쿼리를 사용할 때는 항상 모바일 퍼스트 접근방식으로 디자인합니다.

**5. 애니메이션과 트랜지션 최적화**

- 가능한 브라우저의 리플로우와 리페인트 과정을 발생시키지 않는 `transform`과 `opacity`를 활용해 애니메이션을 구현합니다.
- 두 속성은 `GPU`를 사용해 하드웨어 가속을 제공하며, 이를 활용하면 `CPU` 부담을 줄이고 더욱 부드러운 애니메이션 효과를 제공할 수 있게됩니다.
  - 예를 들어 `transform : translateX(50px)`는 요소를 수평으로 `50px`이동 시키지만, `GPU`를 사용하는 속성이므로, 레이아웃을 다시 계산할 필요없이 효과를 빠르게 처리할 수 있게됩니다.

**6. 코드 최소화**

- 불필요한 속성값을 제거하고, 축약할 수 있는 속성은 축약합니다.
- CSS 파일의 크기를 줄이기 위해, 프로덕션 환경에서는 CSS를 압축합니다.