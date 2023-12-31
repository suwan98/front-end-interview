# Q : 플로트(Floats)에 대해 설명하고, 그들이 어떻게 작동하는지 설명해주세요.

<br />

# A :

**CSS에서의 float 속성은 해당 요소를 다음 요소위에 떠있게합니다**

- 여기서 떠있다는 개념은 요소가 기본 레이아웃 흐름에서 벗어나 요소의 모서리가 페이지의 왼쪽이나 오른쪽으로 이동하게 되는 것 입니다.
- 현재에는 `flex`나 `grid`와 같은 레이아웃 속성으로 인해 잘 쓰이지않는 추세로 알고있지만 과거 레거시코드에서는 `float` 속성이 사용될 수 있으므로 알아둬야합니다.
- 예를들어서, 현재 페이지의 그림이나 문서를 왼쪽이나 오른쪽으로 띄워서 정렬할 때 사용될 수 있습니다.

**float 속성을 사용할 때 주의사항으로는**

- 요소의 위치를 고정 시키는 `postion: absolute`를 사용하면 안됩니다.
  - `float` 속성 자체가 `relative`한 위치를 지정하기 때문에 `postion : absoulte` 속성이 적용되지 않기 때문입니다.
- 또한, `float` 속성 사용 시 해당 요소는 일반적인 레이아웃 흐름에서 벗어나게 되므로 요소의 부모요소는 해당 요소의 높이를 인식하지 못하게되는데, 이경우 부모 요소에 `overflow:hidden` 속성을 부여해 해결할 수 있게됩니다.
