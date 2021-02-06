# box-sizing	



HTML의 모든 요소는 **Box Model**로 표현한다. Box안에는 `content`, `padding`, `border`, `margin`이 포함되어 있다. 여기서 Box의 크기를 정확하게 표현하기 위해 `box-sizing`을 고려해야한다. 이를 위해 다음 두 가지 속성을 설정할 수 있다.

```css
div{
    box-sizing: border-box;
}

div{
    box-sizing:content-box;
}
```



- `content-box` 

기본으로 설정되어있는 속성 값이다. `border`가 1px인 Box의 너비를 100px로 한다면 Box안의 `content`가 100px가 되고, 전체 Box의 너비는 101px이 된다.

즉, Box의 크기 = `content`의 크기 + `border`의 굵기로 결정된다.



- `border-box`

실제로 Box의 너비를 100px를 하기위해서 `border-box`속성을 사용한다. 이 속성은 너비를 100px로 설정하면 `content`너비와 `border`가 합쳐져 100px이 된다.






