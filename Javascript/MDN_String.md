# MDN01 : String Method

> - MDN을 통해 Javascript를 공부한다.
> - Javascript에서 문자열을 위해 내장된 함수를 알아본다.



웹은 사람들이 정보를 교환하고 공유할 수 있도록 설계된 텍스트 기반의 매체이기 때문에 웹에 표시된 단어를 제어하는 것이 중요하다. `Javascript`는 문자열을 조작하기 위한 여러가지 기능을 갖고있다.



`Javascript`는 모든 것이 객체이며 문자열이 생성되면 해당 문자열은 String의 객체가 된다. 따라서 문자열은 String에 포함된 함수를 사용할 수 있게된다.



- **문자열의 길이** : `length`

```javascript
var str = 'abcdefg';
console.log(str.length); // 7이 출력된다.
```



- **특정 문자열 찾기**

대괄호를 통해 문자열의 특정 위치에 접근하여 해당 원소를 출력할 수 있다.

문자열의 마지막 인덱스는 문자열의 길이에 -1이다. 

```javascript
var str = 'abcdefg';
console.log(str[0]); // a가 출력된다.
console.log(str[str.length-1]) // g가 출력된다.
```



- **문자열 내부의 특정 문자열 찾기** : `indexOf()`

어떤 문자열에서 특정 문자열을 알고자 할때는 `indexOf()`를 사용한다.

만약 어떤 문자열 내에서 특정 문자열을 찾았으면 특정 문자열의 처음위치와 맞는 인덱스를 출력한다. 또한 문자열을 찾지 못했다면 `-1`을 출력한다.

```javascript
var str = 'abcdefg';
console.log(str.indexOf('cde')) // 2가 출력된다.
console.log(str.indexOf('pq')) // -1이 출력된다.
```



- **문자열 슬라이싱** : `slice()`

문자열의 특정 부분만 반환하기 위해서 `slice()`를 사용한다.

`slice()`에서 두 번째 인자는 선택사항이며 포함시키지 않는다면 시작위치부터 끝까지 반환한다.

```javascript
var str = 'abcdefg';
var newStr = str.slice(1, 3);
console.log(newStr); // bc가 출력된다.
```



- **대/소문자 변경** : `toLowerCase()` , `toUpperCase()`

문자열의 대문자를 소문자로, 소문자를 대문자로 변경할 수 있다.

이 함수를 사용해도 원본의 문자열은 바뀌지 않는다.

```javascript
var str = 'abcdefg';
console.log(str.toUpperCase()); // ABCDEFG가 출력된다.

var newStr = str.toUpperCase();
console.log(newStr.toLowerCase()); // abcdefg가 출력된다.
```



- **문자열의 일부를 변경** : `replace()`

문자열 내에서 특정 문자열을 다른 문자열로 변경할 수 있다.

이 함수를 사용해도 원본의 문자열이 변경되지는 않는다.

```javascript
var str = 'hi, lee';
var newStr = str.replace('hi', 'hello'); //hi를 hello로 변경
console.log(newStr) // hello, lee가 출력된다.
```

