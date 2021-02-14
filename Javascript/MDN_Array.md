# MDN01 : 배열

> - MDN을 통해 Javascript를 공부한다.
> - 다수의 데이터를 가지고 있는 하나의 객체인 배열을 알아본다.



### 배열 생성하기

- 배열은 `[]`안에 여러 개의 데이터를 담을 수 있다.
- 숫자형과 문자열이 동시에 담길 수도 있다.

```javascript
var arr = [1, 2, 'a', 'b', 'c'];
```



### 배열의 접근과 수정

- 배열의 특정 원소에 접근하기 위해서 배열의 이름과 `[]`을 사용한다.
- 배열의 특정 원소에 접근해서 수정을 할 수도 있다.

```javascript
var arr = [1, 2, 'a', 'b', 'c'];
arr[1] = 'z';
console.log(arr); // [ 1, 'z', 'a', 'b', 'c' ]이 출력된다.
```



### 2차원 배열

- `[]`을 겹쳐 사용하여 2차원 배열을 생성할 수도 있다.
- 또한 문자열이 포함된 1차원 배열에서 문자열의 특정 문자에 접근하기 위해서 `[]`를 두개 사용한다.

```javascript
var numbers = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
console.log(numbers[0][0]); // 1
console.log(numbers[1][0]); // 4
console.log(numbers[2][0]); // 7
```



### 배열의 갯수 알아내기 : `length`

- 배열 내의 원소 수를 알기위해서 `length`함수를 사용한다.
- 아래의 코드는 `numbers`의 2차원 배열이며 3개의 1차원이 원소가 된다.
- `for`문을 사용하여 각 원소에 순차적으로 접근할 수 있다.

```javascript
var numbers = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
console.log(numbers.length) // 3이 출력된다.

for(var i=0; i<numbers.length; i++){
    for(var j=0; j<numbers[i].length; j++){
        console.log(numbers[i][j])
    }
} // 1 ~ 9가 한 줄에 하나씩 출력된다.
```



### 배열과 관련된 내장함수

- `split()` : **문자열을 배열로**

split()안에 들어간 문자를 기준으로 문자열이 나뉘어 배열로 저장된다.

```javascript
var str = 'a b c d';
var arr = str.split(' '); // 빈 칸을 기준으로
console.log(arr); // ['a', 'b', 'c', 'd']가 출력된다.
```



- `join()` : **배열을 문자열로**

join()안에 들어가 문자를 기준으로 배열의 원소들을 문자열로 묶어준다.

```javascript
var arr = ['a', 'b', 'c', 'd'];
var str = arr.join('-');
console.log(str) // a-b-c-d가 출력된다.
```



- `push()` : **배열의 끝에 원소 추가하기**

배열의 끝에 원소를 추가할 수 있다.

```javascript
var number = [1, 2, 3, 4, 5];
number.push(6);
console.log(number) / [1, 2, 3, 4, 5, 6]이 출력된다.
```



- `pop()` : **배열의 끝에있는 원소 삭제하기**

배열의 끝에 있는 원소를 반환하고 삭제한다.

```javascript
var number = [1, 2, 3, 4, 5];
var num = number.pop(); // 배열의 끝에 있는 원소인 5를 반환
console.log(num) // 5가 출력된다.
```



- `unshift()` : **배열 앞에 원소 추가하기**

배열의 앞에 원소를 추가한다.

```javascript
var number = [1, 2, 3, 4, 5];
number.unshift(0);
console.log(number) // [ 0, 1, 2, 3, 4, 5 ]이 출력된다.
```



- `shift()` : **배열의 앞에있는 원소 삭제하기**

배열의 앞에있는 원소를 반환하고 삭제한다.

```javascript
var number = [1, 2, 3, 4, 5];
number.shift();
console.log(number); // [ 2, 3, 4, 5 ]이 출력된다.
```

