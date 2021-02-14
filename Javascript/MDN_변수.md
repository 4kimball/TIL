# MDN01 : 변수

> - MDN을 통해 Javascript를 공부한다.
> - 변수의 의미와 활용에 대해 알아본다.



우리가 웹 브라우저에서 이름을 입력하면 입력된 이름과 함께 'hello'라는 인사를 한다고 하자. 코드의 구성은 다음과 같이 될 것이다.

```html
<button>
    Input Your Name
</button>
```

```javascript
const button = document.querySelector('button')

button.onclick = function(){
    let name = prompt('What is your name?');
    alert('Hello '+name)
}
```

버튼을 클릭했을 때 실행되는 함수를 보면 이름을 입력받아 `name`이라는 변수에 저장한다. 그리고 그 변수에 저장된 이름을 브라우저 상에서 출력하게된다. 

만약 `name`이라는 변수를 사용하지 않는다면 사용자가 입력한 이름을 맞춰야하는 불편함이 존재한다. 

이처럼 변수는 프로그래밍에서 매우 유용하게 쓰이고 있다. 변수에는 문자열, 숫자뿐만 아니라 함수까지 저장할 수 있다.



### 변수의 선언

- 변수를 사용하기 위해서 먼저 변수를 선언해야한다.
- `var`을 통해 변수를 선언할 수 있으며 아래는 `name`이라는 변수를 선언한 것이다.
- 변수에 값을 할당하지 않고 선언만 했을때, 변수에는 `undefined`가 저장되어 있다.

```javascript
var name; 
```



### 변수에 값 할당

- 변수를 선언한 후에 어떠한 값을 할당하여 변수를 초기화할 수 있다.

```javascript
var name = 'kim'
var age;
age = 25;
```



- 또한 이미 초기화된 변수에 다른 데이터를 할당하여 갱신할 수 있다.
  - 그렇게되면 가장 최근에 할당한 데이터가 변수에 저장되어 있다.

```javascript
var name = 'kim'
name = 'lee'
```



### 변수 이름 규칙

- 변수의 이름 앞에 `_`을 사용하지 않는다. 이것은 Javascript에서 특별한 의미를 갖고있기 때문에 혼란을 줄 수 있다.
- 여러 단어를 묶어서 변수명을 지을 때는 `camel case`를 사용한다. 첫 번째 단어는 소문자를 사용하고 두 번째 단어는 대문자로 시작하고 나머지는 소문자를 사용한다.
- Javascript 예약어를 사용할 수 없다.



### 변수의 종류

변수에 저장할 수 있는 데이터가 정해져 있으며 변수에 저장된 값의 데이터 타입을 확실히 알 필요가 있다.

- **Number**

변수에 정수 또는 부동소수점을 저장할 수 있다.

```javascript
var number = 15
var number = 2.5
```



- **String**

변수에 문자열을 할당할 때는 작은따옴표`'` 또는 큰따옴표`"`를 사용한다.

```javascript
var name = 'kim'
var name = "park"
```



- **Booleans**

`true`와 `false`를 갖고있다. 

```javascript
var possible = true
var compare = 5 < 2 // false가 출력된다.
```



- **Arrays**

배열은 `[]`안에 여러 개의 값을 포함시킬 수 있는 객체이다. 

```javascript
var nameArray = ['kim', 'park', 'lee']
var ageArray = [15, 40, 25]
```



배열에 저장된 원소에 접근할 때는 `[]`안에 숫자를 넣어서 사용하며 첫 번째자리는 0부터 시작한다.

```javascript
var nameArray = ['kim', 'park', 'lee']
nameArray[0] // kim
nameArray[2] // lee
```



- **Object**

객체는 실세계의 물체를 모델링하는 것이다. 다음은 강아지 객체를 생성한 것이다.

객체 안에는 `key`, `value`형태로 데이터가 저장되어 있다.

```javascript
var dog = {
    name : 'spot',
    age : 4,
    breed : 'Dalmatian'
};
```



