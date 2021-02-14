# MDN : Object Basic

> - MDN을 참고하여 객체에 대해 공부한다.
> - 객체와 관련된 기본적인 문법을 알아본다.



### 객체 기본

- 객체는 객체와 관련된 데이터와 함수의 집합이다.
  - 객체는 여러 데이터와 함수로 이루어지는데 객체 안에있는 데이터와 함수를 보통 프로퍼티와 메소드라고 부른다.
- 객체는 `{}`를 통해 생성할 수 있다.
- `name`, `age`, `gender`, `interests`는 **프로퍼티**, `bio`, `greeting`은 **메소드**이다.

```javascript
var person = {
  name: ['Bob', 'Smith'],
  age: 32,
  gender: 'male',
  interests: ['music', 'skiing'],
  bio: function() {
    alert(this.name[0] + ' ' + this.name[1] + ' is ' + this.age + ' years old. He likes ' + this.interests[0] + ' and ' + this.interests[1] + '.');
  },
  greeting: function() {
    alert('Hi! I\'m ' + this.name[0] + '.');
  }
};
```



- 위와 같이 객체 리터럴을 사용해서 객체를 생성하는 것은 연속된 국조체나 연관된 데이터를 일정한 방법으로 변환할 때 많이 사용한다.



### 객체 사용하기

- 정의된 객체는 `.`과 `[]`을 통해 사용한다.

```javascript
person.age
person.bio()

person['age']
```



### 객체 멤버 정의하기

- 객체에 정의된 멤버를 호출하기도 하고 객체에 새로운 멤버를 추가할 수 있다.

```javascript
person.location = 'seoul'; // 새로운 멤버 추가
person.age = 25; // 기존의 멤버 수정
```



### this

- `this`는 현재 코드를 실행하고 있는 객체를 가리킨다.

```javascript
greeting: function() {
  alert('Hi! I\'m ' + this.name.first + '.');
}
```

