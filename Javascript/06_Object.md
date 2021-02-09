# 06_Object

> - 자바스크립트에서 객체는 key : value 형태의 프로퍼티들을 저장하는 컨테이너다.
> - 객체를 생성하는 방법은 크게 두 가지가 존재한다.



### 객체의 생성

- 객체를 생성하기 위해서는 `생성자 함수`로 선언하거나 `객체 리터럴`로 만들 수 있다.

```javascript
var foo1 = new Object() // Object() 생성자 함수
var foo2 ={
    name : 'kim'
} // 객체 리터럴 => 주로 리터럴 방식으로 객체 생성
```

- 리터럴 방식을 보면 왼쪽에 key와 오른쪽에 value를 선언한 것을 확인할 수 있으며 `key`는 문자형, `value`는 모든 자료형이 올 수 있다.



### 프로퍼티 접근

- 다음은 프로퍼티에 접근하여 제어하는 방법이다.
- 대괄호를 통해 `key`에 접근할 때는 문자형으로 접근한다.

```javascript
var foo = {
    name : 'kim',
    age : 25
    "user id" : 123 // 여러 단어를 조합할 경우 따옴표 안에 입력한다. 
}

// 프로퍼티 읽기
console.log(foo.name)
console.log(foo.age)

// 프로퍼티 동적 생성
foo.location = 'seoul'
console.log(foo.location)

// 프로퍼티 갱신
foo.age = 35
console.log(foo['age']) // 35 출력
//여러 단어의 조합으로 이루어진 key에 접근할 때 대괄호를 사용

// 프로퍼티 삭제
delete foo.age
console.log(foo.age) // undefined 출력
```



### `in`과 `for - in`을 통한 프로퍼티 검색

- `in`과 `for - in`을 통해 프로퍼티의 존재를 파악할 수 있다.
- 아래의 코드는 `in`을 통해 프로퍼티를 검색하는 것이다.
  - 반드시 `key`를 통해 프로퍼티를 찾을 수 있으며 `key`는 따옴표로 묶어서 검색한다.

```javascript
var user = {
    name : 'alex',
    age : 17
}

console.log("name" in user) // true
console.log("id" in user) // false
```

- 아래의 코드는 `for - in`을 통해 객체 안의 모든 프로퍼티를 파악할 수 있다.

```javascript
var user = {
  name : 'alex',
  age : 17,
  id : '123'
}

for (var key in user){
  console.log(key, user[key])
  // name alex
  // age 17
  // id 123
}
// user.key라고 하면 value값이 undefined가 출력된다.
```

