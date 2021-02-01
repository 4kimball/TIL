# 01_Data Type

> `Javascript`는 느슨한 타입 체크 언어이다. 따라서 변수에 어떤 데이터를 저장하는냐에 따라 변수의 타입이 결정된다. `Javascript`의 자료형 5개를 알아보자.



 ## 1. 숫자형

- `int`, `float` 등이 정해져있는 C언어와 달리 `Javascript`는 모든 숫자를 64비트 부동 소수점 형태로 저장한다. 
- 따라서, 모든 수는 `number` 타입이다.

```javascript
var num = 5
console.log(typeof(num)) // number가 출력된다.
```

- 숫자에 대한 연산을 진행할 때 실수의 연산이 되기 때문에 출력도 실수가 된다.
- 출력 결과가 정수로 나오게 하기 위해서는 `Math.floor()`를 통해 소수 부분을 버린다.ㄴ

```javascript
var num = 7/2
console.log(num) // 3.5가 출력된다.
console.log(Math.floor(num)) // 3이 출력된다.
```

- 일반적인 숫자 이외에 `Infinity` `-Infinity` `NaN` 이 존재한다.
- 이러한 값들 때문에 잘못된 연산을 진행해도 치명적인 오류가 발생하지 않는다.

```javascript
console.log(1 / 0) // 어떠한 정수든 0으로 나누면 무한대가 되며 Infinity가 출력된다.

console.log('1' / 0) // 숫자가 아닌 자료형으로 수학연산을 하면 NaN이 출력된다.
```





## 2. 문자형

- 문자열은 작은 따옴표`'`, 큰 따옴표`"`로 생성한다.
- 문자형은 `string`타입이다.

```javascript
var name = 'name'
var age = "age"

console.log(typeof(name)) // string이 출력된다.
console.log('hello')
```

- 문자열 중간에 변수나 표현식을 삽입하여 출력하기 위해서는 `백틱`과 `${}` 을 사용한다.
- 작은 따옴표나 큰 따옴표는 중간에 변수나 표현식을 삽입할 수 없다.

```javascript
var age = 25
console.log(`나의 나이는 ${age}`) // 나의 나이는 25가 출력된다.
```



### 3. 불린형

- `true` 와 `false`가 존재한다.
- 불린형은 `boolean` 타입이다.

```javascript
console.log(4 > 1) // ture가 출력된다.
```



### 4. null

- `null`은 존재하지않는 값, 비어있는 값 알 수 없는 값을 의미한다.
- null의 타입은 `object`이다.

```javascript
var num = null
console.log(typeof(null)) // object가 출력된다.
```



### 5. undefined

- 기본적으로 값이 할당되지 않은 변수는 `undefined`이다.
- `null`과 같이 값이 비어있음을 나타내지만 `undefined`는 타입이고 값을 나타낸다.

```javascript
var empty
console.log(typeof(empty)) // undefined가 출력된다.
```

