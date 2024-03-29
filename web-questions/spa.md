# Q : CSR과SSR의 차이점에 대해서 설명해주세요.

<br />

# A : CSR과 SSR의 가장 큰 차이점은 어디서 렌더링을 진행하냐에 따라 차이가 생깁니다.

**CSR의 경우 말그대로 클라이언트 측에서 모든 렌더링이 이루어집니다.**

- 이로인해 초기로딩 속도는 상대적으로 SSR보다 느리지만, 모든 리소스를 한번에 받아오게 되므로, 이후 페이지 이동은 빠르게 처리됩니다.
- CSR은 또 다른 약점이 존재하게 되는데, CSR 방식에서는 초기에 빈 HTML을 불러와 이후 JavaScript를 통해 동적으로 렌더링을 진행합니다. 이 과정에서 검색 엔진이 페이지를 크롤링 할때 JavaScript가 완전히 로드되지 않은 상태를 크롤링할 가능성이 있어, SEO에 부정적인 영향을 끼칠 수 있습니다.

<br />

**SSR은 서버에서 HTML을 생성 후 클라이언트로 보내주는 방식입니다. 이로인해 초기 로딩 속도는 CSR에 비해 빠르지만, 페이지가 이동할 때마다 새로운 HTML을 요청하므로, CSR보다 페이지 이동이 느려질 수 있습니다.**

- 반면 SEO 관점에선 유리한데 그 이유는 HTML이 이미 서버에서 완전히 렌더링 된 상태로 클라이언트에 전달되므로 검색엔진이 페이지를 크롤링 할때 완전한 내용을 크롤링할 수 있게됩니다.
