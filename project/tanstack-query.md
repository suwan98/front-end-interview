# Q : Tanstack-Query란 무엇이며 이를 사용하는 이유는 무엇일까요?

<br />

# A : Tanstack-query란 애플리케이션 상태 중 서버에서 패치된 상태를 관리할 때 사용되는 라이브러리입니다.

### Tanstack-Query를 사용하는 이유는 다음과 같습니다.

1. 데이터 패치와 캐싱

- Tanstack-Query는 데이터 패치와 캐싱을 자동으로 처리해줍니다.
- 이를 통해 개발자는 사용자는 패치된 데이터, 에러 객체, isLoading 상태등을 손쉽게 얻을 수 있게됩니다.
- 또한 데이터를 패칭할때 캐싱 옵션을 통해 해당 데이터를 캐싱할 수 있게되 사용자에게 캐싱된 데이터를 보여줄 수 있게됩니다.

2. 동기화

- Tanstack-Query는 서버와 클라이언트 사이의 데이터 동기화를 자동으로 처리해줍니다.

3. 미들웨어를 통한 디버깅

- React Query Devtools를 통해 캐시로 저장되는 데이터의 정보를 개발자가 육안으로 확인할 수 있습니다.
