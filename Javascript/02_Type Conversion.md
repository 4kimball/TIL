# 02_형 변환 - Type Conversion



### 1. 숫자형으로 변환

- 다음과 같이 숫자의 연산과 관련된 함수와 표현식을 사용할 때 자동으로 형 변환이 일어난다. `암시적 형변환`

```javascript
var num = '5'/'2'
console.log(num) // 2.5가 출력된다.
console.log(typeof(num)) // num의 타입은 number가 된다.
```



- 위와 같이 자동으로 형변환이 일어날 경우도 있고 `Number()`를 통해 사용자가 직접 숫자형으로 변환시킬 수 있다. `명시적 형변환`
- 웹에서 문자 기반의 숫자를 입력받을 때 사용된다.

```javascript
var str = '1234'
var num = Number(str)

console.log(str)
console.log(typeof(str)) // 숫자형으로 변환하기 전에는 string이 출력된다.
console.log(num)
console.log(typeof(num)) // 숫자형으로 변환 후에 number가 출력된다.
```



- 숫자 이외의 문자가 들어있으면 `NaN`을 출력한다.

```javascript
var str = '안녕 1234'
var num =Number(str)

console.log(num) // NaN이 출력된다.
console.log(typeof(num)) // 타입은 number가 출력된다.
```



- 숫자형으로 변환 시 적용되는 규칙
  - `undefined` -> `NaN`
  - `null` -> `0`
  - `true and false` -> `1` 과 `0`
  - `string` -> 문자열의 처음과 끝의 공백을 제거 후, 문자열이 없다면 `0`을 있다면 문자열에서 숫자를 읽는다. 반환에 실패하면 `NaN`이 된다.



### 2. 문자형으로 변환

- 문자형으로 변환하기 위해서 `String()`을 사용한다.

```javascript
var num = 1234
var str =String(num)

console.log(num)
console.log(str)
console.log(typeof(str)) // string이 출력된다.
```



### 3. 불린형으로 변환

- 불린형으로 변환하기 위해서 `Boolean()`을 사용한다.
- `0`, `null` , `undefined` , `NaN`는 `false`가 반환되며 그 외의 값은 `true`가 반환된다.

```javascript
var a = ""
var b = 10
var c = NaN

console.log(Boolean(a)) // false
console.log(Boolean(b)) // true
console.log(Boolean(c)) // false
```

