# Bootstrap : Spacing

> Bootstrap에서 `padding`과 `margin`을 어떻게 사용하는지 알아본다.



- `m` : margin을 의미한다.
- `p` : padding을 의미한다.



### Sides

`padding`과 `margin`을 적용하는 방향은 다음과 같다.

- `t` : margin-top **or** padding-top
- `b` : margin-bottom **or** padding-bottom
- `s` : margin-left **or** padding-left
- `e` : margin-right **or** padding-right
- `x` : -left **and** -right
- `y` : -top **and** -bottom



### Size

기본적인 단위는 `rem`을 사용한다.

- `0` : margin 또는 padding을 0으로 설정
- `1` :  margin 또는 padding을 `0.25rem`으로 설정
- `2` : margin 또는 padding을 `0.5rem`으로 설정
- `3` : margin 또는 padding을 `1rem`으로 설정
- `4` : margin 또는 padding을 `1.5rem`으로 설정
- `5` : margin 또는 padding을 `3rem`으로 설정
- `auto` : **margin**을 `auto`로 설정

```html
<div class="mx-auto my-0">
    example
</div>
```



