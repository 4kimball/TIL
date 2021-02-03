# Bootstrap : Postion

> Bootstrap에서 Postion을 설정하는 방법에 대해 알아본다.



Postion의 속성을 사용하기 위해서 다음과 같이 사용한다.

- `position-relative` 
- `position-absolute` 
- `position-absolute top-10 start-10` : start는 왼쪽 end는 오른쪽을 나타낸다.
- `fixed-top` , `fixed-bottom` : 위 또는 아래에 고정되어 있는다.
- `sticky-top` : 다음과 같이 설정되어 있다.

```css
position: -webkit-sticky;
position: sticky;
top: 0;
z-index: 1020;
```

