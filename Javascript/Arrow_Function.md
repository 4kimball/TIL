# 화살표 함수



- **Arrow function 기본**

Arrow function은 다음과 같이 사용할 수 있으며 인자 `n`을 받는 함수 `func`가 생성된다. 여기서 `func`는 화살표(`=>`) 오른쪽에 있는 표현식을 계산하여 결과를 반환한다. 

정리하면 `=>` 왼쪽에 있는 인자를 이용하여 오른쪽의 표현식을 계산하는 함수이다.

```javascript
var func = n => n*2
console.log(func(2)) // 4가 출력된다.
```

```javascript
var sum = (x, y) => x+y
console.log(sum(3,5)) // 8이 출력된다.
```



- **여러 줄의 구문을 평가하는 화살표 함수**

위에서처럼 한 줄이 아닌 여러 줄을 작성할 때는 중괄호`{}`안에 함수를 정의한다. 만약 중괄호를 사용하여 함수를 정의했다면 `return`값을 반환해줘야 한다.

반환해주지 않으면 `undefined`가 반환된다.

```javascript
var sum = (a, b) =>{
  result = a+b
  return result
}

console.log(sum(3,5)) // 8이 출력된다.
```

