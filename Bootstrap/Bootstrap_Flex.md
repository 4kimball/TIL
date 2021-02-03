# Bootstrap : Flex

> Bootstrap에서 flex를 사용하는 방법을 알아본다.



기본적으로 `flex`를 활용하기 위해서 `d-flex`라는 class를 사용한다. 이는 `display: flex`를 줄인 것이며 `d-block`는 `display: block`를 의미한다.



다음은 컨테이너에 포함된 `flex-item`을 제어하는 class이다.

- `flex-row` , `flex-column` : `flex-direction`을 **row** 또는 **column**으로 설정한다.

  

- `justify-content-start` , `justify-content-center` , `justify-content-end` : `justify-content`를 통해 오른쪽, 가운데, 왼쪽으로 배치한다.

- `justify-content-between` , `justify-content-around` , `justify-content-evenly` : `justify-content`를 통해 요소들을 일정하게 정렬한다.



- `align-items-start` , `align-items-center` , `align-items-end` : `align-items`를 통해 corss axis에 있는 요소들을 정렬한다.
- `align-self-start `, `align-self-center`, `align-self-end` : `align-self`를 통해 컨테이너에 속한 개별 요소들을 정렬시킬 수 있다.



- `flex-nowrap` , `flex-wrap` , `flex-wrap-reverse` : `flex-wrap`으로 컨테이너의 범위를 넘어가는 요소들을 안에서 정렬시킬 수 있다.



*이 외의 다른 속성도 Bootstrap에 포함되어 있으며 공식문서를 참고하도록 한다.*