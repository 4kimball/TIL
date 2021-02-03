# Display

> `display`는 **CSS** 속성 중의 하나로 요소를 `block`  또는 `inline`으로 처리하고, 자식 요소를 `flow` , `grid` , `flex` 로 배치할 때 사용한다.



HTML의 요소들은 기본적으로 `block` 레벨 또는 `inline` 레벨 속성을 갖고 있다. `div`는 대표적인 `block` 레벨 요소이며 `span`은 대표적인 `inline` 레벨 요소이다.



### block

- `block` 레벨은 한 줄을 모두 차지한다. 따라서 `block` 레벨을 갖는 요소 다음의 요소는 다음 줄에 생성된다.
- `block` 레벨 요소 안에 `inline` 레벨 요소가 들어갈 수 있다.
  - `inline`레벨 요소에 `block` 레벨 요소가 들어가지는 못한다.
- `block`의 `margin-top` 과 `margin-bottom` 은 가장 큰 한쪽의 마진으로 상쇄된다.



### inline

- 한 줄에서 일부의 칸을 차지한다.
- 줄바꿈이 일어나지 않으면 `inline` 레벨의 요소를 한 줄에 여러개 생성할 수 있다.
- **content**의 너비만큼 width의 크기가 결정된다.
- `width` , `height` , `margin-top` , `margin-bottom` 을 지정할 수 없다.
  - 상하의 여백을 지정할 때 `line-height`로 지정한다.



### inline-block

- `inline`처럼 텍스트 흐름대로 나열하지만 `block`형태도 포함되어 있기 때문에 `block`과 관련된 속성을 지정할 수 있다.



### none

- 해상 요소가 화면에서 사라지고 요소의 공간도 없어지게 된다.
- `visibility: hidden` 은 화면에서 사라지지만 공간은 없어지지 않는다.