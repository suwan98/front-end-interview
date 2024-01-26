# Q : nextjs의 useTheme을 통해 다크모드를 구현하셨다고하는데, 어떤방식으로 구현하셨나요?

<br />

# A : next-themes와 tailwindCSS를 조합해서 구현했습니다.

- ThemeProvider 컴포넌트를 만든 후 layout 파일에 래핑했습니다.
- useTheme hook을 통해 systemTheme, theme, setTheme를 불러왔습니다. 그리고 현재 테마는 시스템 테마인지 아닌지를 판단하여 currentTheme에 저장합니다.
- useEffect를 통해 컴포넌트가 마운트되었는지 확인하고, 마운트되었다면 현재 테마가 'dark'인 경우와 아닌 경우에 따라 다른 버튼을 렌더링합니다. 'dark'인 경우에는 햇빛 아이콘을 가진 버튼을 렌더링하고, 이 버튼을 클릭하면 setTheme을 통해 테마를 'light'로 변경합니다. 반대로 'dark'가 아닌 경우에는 달 아이콘을 가진 버튼을 렌더링하고, 이 버튼을 클릭하면 테마를 'dark'로 변경합니다.
