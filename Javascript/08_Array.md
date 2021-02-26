# 08. Array

> 객체는 순서를 고려하지 않는 자료구조이기 때문에 새로운 프로퍼티를 기존 프로퍼티 사이에 끼워 넣는 것이 불가능하다. 이럴 때 순서가 있는 자료구조인 `배열`을 사용한다.



### 배열 생성

- 다음은 빈 배열을 생성하는 방법이다.

```javascript
var arr = new Array();
var arr = [];
```

- 데이터를 포함하여 생성할 수도 있다.

```javascript
var numbers = [1, 2, 3, 4]
```



### 인덱싱

- 선언되 배열의 각 요소에 접근하기 위해서 `[]`안에 요소의 인덱스를 포함시킨다.
- 다른 언어들과 마찬가지로 인덱스는 0부터 시작한다.

```javascript
var numbers = [1, 2, 3, 4]
console.log(numbers[1]) // 2
console.log(numbers[3]) // 4
```

- 인덱스를 활용해 데이터를 수정하고 추가할 수 있다.
- 현재 아래의 `numbers`라는 배열은 인덱스가 2까지 존재하는데 인덱스 5에 데이터를 추가하면 중간 인덱스인 `3`과 `4`가 빈자리로 되고 그 뒤에 데이터가 추가된다.
- 사이에 빈 데이터를 출력하면 `undefined`가 출력된다.

```javascript
var numbers = [1, 2, 3]
numbers[1] = 9
numbers[5] = 10
console.log(numbers) 
// [ 1, 9, 3, <2 empty items>, 10 ]
console.log(numbers[3]) // undefined
```



### Array.length

- 배열에 포함된 요소들의 개수를 파악하기 위해서 `length`를 사용한다.

```javascript
var location = ['서울', '대전', '부산']
console.log(location.length) // 3이 출력된다.
```



### pop & push

- 배열의 끝에 있는 요소를 제거하고, 제거한 요소를 반환하기 위해서 `pop`을 사용한다.

```javascript
var location = ['서울', '대전', '부산']
var name = location.pop()
console.log(name) // 부산
console.log(location) // ['서울', '대전']
```

- 배열 끝에 요소를 추가하기 위해서 `push`를 사용한다.

```javascript
var location = ['서울', '대전', '부산']
location.push('광주')
console.log(location) // [ '서울', '대전', '부산', '광주' ]
```



### shift & unshift

- 배열의 앞에 요소를 제거하고, 제거한 요소를 반환하기 위해서 `shift`를 사용한다.

```javascript
var numbers = [1, 2, 3, 4]
var num = numbers.shift()
console.log(num) // 1
console.log(numbers) // [2, 3, 4]
```

- 배열 앞에 요소를 추가하기 위해서 `unshift`를 사용한다.
- 또한 한 번에 많은 데이터를 추가할 수도 있다.

```javascript
var numbers = [1, 2, 3, 4]
numbers.unshift(10)
console.log(numbers) // [ 10, 1, 2, 3, 4 ]
```

```javascript
var numbers = [1, 2, 3]
numbers.unshift(10, 9)
numbers.push(7, 8)
console.log(numbers) // [10, 9, 1, 2, 3, 7, 8]
```

