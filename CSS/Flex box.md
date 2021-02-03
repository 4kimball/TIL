# Flex box

> `flex`는 자신의 컨테이너의 공간에 맞게 item들의 위치를 제어한다.. `flex`의 속성들을 통해 유연하게 배치하고 정렬할 수 있다.



### 1. main axis & cross axis

- 아래와 같이 컨테이너를 `flex`를 지정하면 `main axis`와 `cross axis`가 생성될 것이다.

```css
div{
    display: flex;
}
```

- 컨테이너 안에는 여러 개의 item이 존재하며 각 item은 `main axis`를 기준으로 정렬된다. 기본적으로 `row`로 정렬된다.
- 하지만 `flex-direction`을 통해 `main axis`의 방향을 `column`으로 변경시킬 수 있다. 이때 `main axis`는 `column`이 되고 `cross axis`는 `row`가 된다.
- 각각의 item들은 **container 가 제어**하는 것이다.

![image-20210203101634293](C:\Users\2018\AppData\Roaming\Typora\typora-user-images\image-20210203101634293.png)

> ※출처 : https://developer.mozilla.org/ko/docs/Learn/CSS/CSS_layout/Flexbox



### 2. Flex box에 적용할 수 있는 속성

- **배치 방향 설정**: `flex-direction`
- **main axis 기준 정렬**: `justify-content` 
- **cross axis 기준 정렬**: `align-items` , `align-content` , `align-self`
- **기타**: `flex-grow` , `flex-wrap`, `flex-flow` , `flex-basis` , `order` 등



### 3. justify-content

- `main axis`를 기준으로 `flex-item`들을 정렬한다.
  - `space-between` : 요소들 사이에 균등한 간격으로 배치한다.
  - `space-around` : 요소들의 앞, 뒤 공간을 균등하게 분배한다.
  - `space-evenly` : 요소들 사이를 균등한 간격으로 배치하는데 첫 번째요소의 앞과 마지막 요소의 뒤에도 공간을 둔다.
  - `flex-start` : 요소들을 `main axis`를 기준으로 시작점에 배치한다.
  - `center` : 요소들을 가운데에 배치한다.

### 4. align

- `align`이라는 속성은 `cross axis`를 기준으로 `flex-item`을 정렬한다.
- `align`의 종류는 다음과 같다.
  - `align-items` : 한 줄에 포함된 요소들을 배치한다.
  - `align-content` : 여러 줄에 포함된 요소들을 배치한다.
  - `align-self` : 개별 요소들을 각각 배치한다. (container가 아닌 item에서 속성을 적용한다.)