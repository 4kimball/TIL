# Selector

> CSS에서 선택자는 HTML의 요소를 대상으로 스타일을 지정하기 위해 사용된다. 여러가지 선택자에 따라 적용되는 것이 달라지기 때문에 정확하게 파악해야 한다.



### 선택자란?

선택자는 아래의 코드처럼 HTML 요소를 선택하여 CSS 속성값을 적용시킨다. 선택자는 요소를 직접 선택하는 것과 `class` , `id` 를 지정하여 선택하는 방법 등이 있다.

```CSS
h1{
    color: red;
}
```



### 선택자의 종류

- `HTML 요소`

HTML의 태그를 직접 선택하여 CSS 속성 값을 설정한다.

```css
div{
    background-color: blue;
}
```



- `.class`

HTML의 태그의 속성으로 class를 정의할 수 있으며 이를 활용해 CSS 속성 값을 설정할 수 있다. 

```css
.class{
    color: orange;
}
```



- `#id`

HTML의 태그에는 class뿐만 아니라 id를 설정할 수 있으며 id를 선택하여 CSS 속성 값을 설정할 수 있다. 중복된 요소 중 특정 요소만 다른 스타일을 적용할 때 사용할 수 있다.

```css
#id{
    color: green;
}
```



- `우선순위`
  - `id > class > HTML 태그 > 소스순서`
  - 더 구체적일수록 우선순위가 높다.



### Pseudo-classes & Pseudo-elements

- `pseudo-classes`

요소의 **특정 상태**를 스타일링한다. 대표적인 것이 `:hover`가 있으며 마우스 포인터에 따라 요소에 CSS 속성 값을 적용시킬 수 있다.

```CSS
li:hover{
    background-color: blue;
}
```



- `pseudo-elements`

요소의 특정 부분을 선택하여 CSS 속성 값을 적용시킬 수 있다. 아래 코드는 요소 내부의 `p`태그 중 첫 번째 텍스트 라인을 선택하게 된다.

```css
p::first-line{
    color: yellow;
}
```



### 결합자 Combinators

- **자손 결합자**

A` ` B : A요소와 B요소가 공백으로 구분되어져 있으며, A의 모든 자식 요소 중 B와 일치하는 요소를 선택한다.

- **자식 결합자**

A`>` B : A의 자식 요소 중 바로 밑에 있는 B요소를 선택한다.

- **일반 형제 결합자**

A`~` B : A의 형제 요소 중 A 뒤에 위치하는 B요소를 모두 선택한다.

- **인접 형제 결합자**

A`+` B : A의 형제 요소 중 A 바로 뒤에 위치하는 B요소를 선택되지만 A와 B 사이에 다른 요소가 존재하면 선택되지 않는다.

