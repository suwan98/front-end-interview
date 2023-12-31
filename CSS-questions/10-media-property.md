# Q : 스크린 외에 다른 @media 속성의 예시를 들 수 있나요?

<br />

# A : @media 쿼리로 반응형 웹 애플리케이션 구현외에도, 다크모드/라이트모드 구현이 가능합니다.

- 해당 기능은 `prefers-color-scheme 미디어 쿼리`인데, 이를 통해 운영체제에서 설정된 다크모드/라이트모드를 실시간으로 감지해 최적화 된 스타일을 제공할 수 있습니다.

```css
@media (prefers-color-scheme: light) {
  /* 라이트 모드에 적용할 스타일 정의 */
}

@media (prefers-color-scheme: dark) {
  /* 다크 모드에 적용할 스타일 정의 */
}
```
