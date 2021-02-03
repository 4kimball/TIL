# 03_연산자



### 1. 수학 연산자

- `+` 

```javascript
var result = 5+2
console.log(result) // 7이 출력된다.
```

```javascript
var result = 'my'+'name'+'is'
console.log(result) // mynameis가 출력된다.
```

```javascript
var result = '7'+2
console.log(result) // '72'가 출력된다.
console.log(typeof(result)) // String이 출력된다.
```

- `-`

```javascript
var result = 7-3
console.log(result) // 4가 출력된다.
```

- `*`

```javascript
var result = 6*3
console.log(result) // 18이 출력된다.
```

- `/`

```javascript
var result1 = 10/2
var result2 = 7/3

console.log(result1) // 5가 출력된다.
console.log(result2) // 2.3333333333333335이 출력된다.
```

- `%`

```javascript
var result = 5%2
console.log(result) // 1이 출력된다.
```

- `**`

```javascript
var result = 2**3
console.log(result) // 8이 출력된다. 거듭제곱 연산
```

- `+`는 문자열을 연결하는 기능도 있다. 이 외의 다른 연산자는 문자열로 연산을 했을 때 숫자형으로 변형되어 연산 결과가 출력된다.
- `+`는 **Number()**역할도 할 수 있다.
  - `console.log(+'2')` 는 숫자형 2가 출력된다. 문자열 앞에 `+`을 붙이면 문자형이 숫자형이 된다.



### 2. 증감 연산자

- `++` 는 증가 연산자이며 변수에 저장된 숫자를 1증가 시킨다.

```javascript
var num = 5
num++
console.log(num) // 1증가한 6이 출력된다.
```

- `--`는 감소 연산자이며 변수에 저장된 숫자를 1감소 시킨다.

```javascript
var num = 5
--num
console.log(num) // 1감소한 4가 출력된다.
```

- 전위형 vs 후위형
  - `++count` 와 같이 변수 앞에 증감 연산자가 오는 것을 **전위형**이라 하며 변수에 저장된 수를 1증가시켜 다음 변수에서 사용한다.
  - `count--`처럼 변수 뒤에 증감 연산자가 오는 것을 **후위형**이라 하며 다음에 사용될 때 1증가시킨다.



### 3. 비트 연산자

- `&`: AND
- `|` : OR
  - `단축평가` : AND의 경우 두 개의 수가 True일 때 True가 된다. 따라서 앞이 False이면 바로 값을 반환하며 OR의 경우 둘 중 하나라도 True일 때 True이므로 앞이 True면 바로 값을 반환한다.
- `^` : XOR
- `~` : NOT
- `<<` : 왼쪽 시프트
  - `<< N`일 때 해당 수에 2의 N승을 곱하게 된다.
- `>>` : 오른쪽 시프트
  - `>>N`일 때 해당 수에 2의 N승을 나누게 된다.