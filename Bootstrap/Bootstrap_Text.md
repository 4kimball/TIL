# Bootstrap : Text

> Bootstrap에서 Text와 관련된 class를 알아본다.



### Text alignment

아래의 class는 `text-align`의 속성을 갖고있다. 이 속성은 `block level`의 요소 안에 있는 text의 **가로 정렬**을 설정한다.  *(세로 정렬은 `vertical-align`)*

- `text-start` : 가장 왼쪽에 배치된다.
- `text-center` : 가운데에 배치된다.
- `text-right` : 가장 오른쪽에 배치된다.



### Font size

Font size의 약자인 `fs`로 시작하며 내부적으로 `font-size`의 속성을 갖고있다. 크기는 `calc()`를 활용하여 rem과 뷰포트의 너비를 기준으로 설정된다.

`fs-1` ~ `fs-6`이 존재한다.

- `fs-1` 

```css
font-size: calc(1.375rem + 1.5vw) !important;
```

- `fs-2`

```css
font-size: calc(1.325rem + 0.9vw) !important;
```

- `fs-3`

```css
font-size: calc(1.3rem + 0.6vw) !important;
```



### Text color

텍스트에 색상을 설정할 수 있으며 내부적으로 `color`로 설정되어 있다. 기본적인 색상을 알아본다.

- `text-primary` : 파란색
- `text-success` : 초록색
- `text-danger` : 빨간색
- `text-dark` : 검정색
- `text-light` : 하얀색



### Font weight

Font weight의 약자인 `fw`로 시작하며 내부적으로 `font-weight`로 설정되어 있다.

- `fw-bold` : 텍스트를 굵게 설정한다.
- `fw-light` : 텍스트를 얇게 설정한다.



### Text decoration

텍스트에 효과를 넣을 수 있다. 내부적으로 `text-decoration`으로 설정되어 있다.

- `text-decoration-underline` : 텍스트에 밑줄이 생긴다.
- `text-decoration-line-through` : 텍스트 중간에 줄이 생긴다.
- `text-decoration-none` : `a`와 같이 기본적으로 설정되어 있는 설정을 제거할 수 있다.