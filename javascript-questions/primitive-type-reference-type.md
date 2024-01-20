# Q : 원시값과 참조값의 차이점을 메모리 관점에서 설명하라

<br />

# A : 원시값은 메모리에 값 자체가 직접 저장되며, 참조값은 메모리 주소를 저장합니다.

- 원시값은 변수에 값이 직접 저장되는 Call-by-Value 방식으로 값 자체를 복사합니다.
- 참조값은 변수에 객체의 메모리 주소가 저장됩니다.
  - 이러한 방식은 Call-by-Reference, 참조에 의한 전달을 뜻합니다.
  - 이로 인해 참조 값을 가진 변수의 변경은 원본과 복사본 모두에 영향을 끼칠 수 있습니다.