# Q : e.target과 e.currentTarget의 차이점에 대해 설명해주세요.

<br />

# A : 둘은 이벤트 발생 시 참조하는 대상이 서로 다릅니다.

1. e.target은 실제로 이벤트가 발생한 요소를 가리킵니다.
2. e.currentTarget은 현재 이벤트를 처리하고 있는 요소를 가리킵니다. 이는 이벤트 핸들러가 바인딩되어 있는 요소를 뜻합니다.

- 예를 들어 ul요소에 이벤트핸들러가 바인딩되어있고, 내부에 여러개의 li요소가 있다고 가정할때, 특정 li요소를 클릭하면, e.target은 클릭된 li요소를 나타내고, e.currentTaget은 바인딩되어있는 부모요소 핸들러인 ul 태그를 가리킵니다.
