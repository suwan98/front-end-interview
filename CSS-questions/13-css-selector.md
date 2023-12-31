# Q : 브라우저가 CSS 선택자와 일치하는 요소를 어떻게 결정하는지 설명해주세요.

<br />

# A :브라우저는 선택자의 가장 오른쪽 부분부터 시작하여 왼쪽으로 이동하면서 일치하는 요소를 찾습니다.

**최종적으로 렌더트리가 완성되면, 브라우저는 각 CSS 선택자를 렌더트리의 요소들과 비교해 일치하는 요소를 결정합니다**

- 브라우저는 선택자의 가장 오른쪽에 있는 키워드 즉, 가장 구체적인 요소부터 시작합니다.
- 그리고 렌더트리에서 해당 키워드와 일치하는 모든 요소를 찾습니다.
- 선택자의 왼쪽에 있는 상위 요소들과의 일치여부를 확인합니다.
- 이 과정을 거쳐 최종적으로 전체 선택자에 일치하는 요소들이 결정됩니다.
  - 선택자의 특이성, 소스순서, 상속 규칙등을 고려해 최종스타일이 결정됩니다.
