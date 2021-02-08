# 05_Function

> - 자바스크립트에서 함수도 일반 객체처럼 값으로 활용할 수 있다. 따라서 함수를 변수에 할당할 수도 있다.
>
> - 함수는 한 가지의 기능만 담당할 수 있도록 만들어야 하며 함수의 이름에서 그 기능을 파악할 수 있도록 하자.



### 함수 선언문

- 자바스크립트는 함수를 생성하는 방법이 3가지가 있다.
  - 함수 선언문
  - 함수 표현식
  - Function() 생성자 함수
- 다음은 함수 선언문으로 함수를 생성한 것이다.
- 자바스크립트에서 함수는 `function`이라는 키워드로 시작하며 다음에 함수명이 온다.
- 하지만 **리터럴 방식**에서 함수명을 사용하지 않을 수 있으며 이를 **익명 함수**라 부른다.

```javascript
function hello(){
  console.log('hello')
}

hello()
```



### 지역 변수와 외부 변수

- 함수 내부에서 선언한 **지역 변수**는 함수 외부에서 접근할 수 없다.

```javascript
function ChanegeName(){
  var name = 'lee'
}

ChanegeName()
console.log(name) // ReferenceError: name is not defined
```

- 함수 내부와 외부에 똑같은 이름의 변수를 선언하고 함수 내부에서 사용하면 지역 변수에 접근한다.

```javascript
var name = "kim"

function hello(){
  var name = "lee"
  message = "I am"+" "+name
  console.log(message)
}

hello() // 함수 내부에서 선언한 name인 lee에 접근한다.
```



- 함수 외부에서 선언한 **외부 변수**는 함수 내부에서 접근하고 수정도 할 수 있다.

```javascript
var name = "kim"

function ChangeName(){
    name = "lee" // 함수 외부에서 선언한 name 변수 수정
}

ChangeName()
console.log(name) // lee 출력
```



### 매개변수

- 함수를 선언할 때 매개변수를 정의하여 함수를 호출할 때 인자를 전달하여 함수 내부에서 사용할 수 있다.

```javascript
function sum(a, b){
  console.log(a+b)
}

sum(2, 5) // 7이 출력된다.
```



### 기본인자

- 매개변수를 포함한 함수를 호출할 때 매개변수의 수만큼 인자를 전달하지 않으면 `undefined`가 할당된다.
- 다음은 두 개의 정수를 입력받아 합을 출력하는 함수이다. 이때 한 개의 정수만 전달하면 b에 `undefined`가 할당되어 최종 출력결과인 `NaN`이 출력된다.

```javascript
function sum(a, b){
  console.log(a+b)
}

sum(2) // NaN이 출력된다.
```

- 위와 같은 경우에서 값을 전달받지 못했을 때를 대비하여 매개변수에 기본값을 설정할 수 있다.
- 기본값을 설정하면 인자를 전달받지 못했을 때 기본값에 저장된 데이터를 활용한다.

```javascript
function sum(a, b=10){ //b에 10이라는 기본값을 설정하였다.
  console.log(a+b)
}

sum(2) 
// 두 개의 매개변수 중 한 개의 매개변수만 전달
// b에 할당된 10을 활용하여 2+10을 출력하게 된다.
```



### 함수의 반환

- 함수는 `return`을 통해 값을 반환할 수 있다.
- `return`은 함수 내에 어디에서든 선언할 수 있으며 그 순간 함수가 종료된다.

- 다음 `sum()`은 두 수의 합을 반환하는 함수이다.
- `return`값이 없다면 `undefined`를 반환한다.

```javascript
function sum(a, b=10){
  return a+b
}

var result = sum(2, 7) // sum()함수는 return이 있기 때문에 반환될 값을 저장할 변수를 선언해야 한다.
console.log(result)// 함수에서 반환된 값이 result에 저장되어있고 9가 출력된다.
```

