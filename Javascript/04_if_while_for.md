# 04_제어문과 반복문



## :question: 제어문

### 1. `if`

- `if()`의 형태로 `()`안의 조건이 **true**일 때 실행된다.

```javascript
var num = 5

// num에 할당된 값을 2로 나누었을 때 나머지가 1이면 홀수로 판단
if(num%2){
    console.log('홀수입니다.')
}
```



- `if`문의 `()`안에 표현된 것을 **boolean**형으로 변환하여 판단한다.
  - `0`, `""`, `null`, `undefined`, `NaN`은 모두 `false`형태로 변환된다.
  - 위의 값 외에는 모두 `true`형태로 반환된다.
- 아래의 코드는 `true`일 때 `if`문에 있는 문자열이 출력되고, `false`면 `else`문이 출력되는 구조이다.

```javascript
var name = ""
if(name){
    console.log('빈 문자열이 아닙니다.')
}
else{
    console.log('빈 문자열입니다.')
}
// 빈 문자열은 false형이기 때문에 else문이 출력된다.
```



- `else if`를 통해 여러 개의 조건을 만들 수 있다.
- 아래의 코드는 특정 달이 어떤 계절인지 알아보는 코드이다.
  - `&&`는 **AND**연산자, `||`는 **OR**연산자, `!`는 **NOT**연산자이다.

```javascript
var month = 4

if(month>=3 && month<=5){
    console.log('봄 입니다.')
}
else if(month>=6 && month<=8){
    console.log('여름 입니다.')
}
else if(month>=9 && month<=11){
    console.log('가을 입니다.')
}
else{
    console.log('겨울 입니다.')
}
```



### 2. 조건부 연산자 `?`

- 조건 `?`  true : false
  - 조건이 참이면 true가 실행, 거짓이면 false가 실행된다.
- 아래의 코드는 조건부 연산자를 통해 홀짝을 구분하는 것이다.
- `num%2`의 값이 1이면 `?` 홀수이고 아니면`?` 짝수

```javascript
var num = 12
console.log(num%2 ? '홀수' : '짝수')
// 짝수를 출력한다.
```





## :factory: 반복문



### 1. `while`

- `while (조건)`에서 조건이 참이면 계속 반복된다.

```javascript
var num = 5
while(num != 0){
  console.log(num)
  num--
}
// 5 4 3 2 1을 한 줄씩 출력 후에
// 1에서 0이 되었을 때 반복문이 종료된다.
// 한 번씩 반복을 할 때마다 조건을 검사한다.
```



### 2. `for`

- `for(시작점; 반복조건; 증감)` 

```javascript
for(var i=0; i<5; i++){
    console.log(i)
}
// 0 1 2 3 4가 한 줄씩 출력된다.
// i가 0부터 시작해서 1씩 증가하며
// i가 5미만일 때까지 반복한다.
```

- `continue`와 `break`사용하기
  - `continue`는 아래의 코드를 실행하지 않고 다음 스텝으로 넘어간다.
  - `break`는 아래의 코드를 실행하지 않고 반복문을 **종료**한다.

```javascript
for(var i=1; i<11; i++){
    if(i%2) continue;
    // i를 2로 나눈 값이 1이면 아래의 코드는 실행하지 않고
    // 다음 i에 대해 실행한다.
    
    if(i==6) break;
    // i가 6이 되었을 때 break하여 아래의 코드는 실행하지 않고
    // 반복문이 바로 종료된다.
    console.log(i)
}
// 위의 반복문은 2 4가 한 줄씩 출력된다.
```

