# 07_Method

> 객체의 프로퍼티에 함수를 할당해 객체에게 어떠한 동작을 할 수 있도록 한다.



### Method 생성

- `함수 표현식`으로 생성 후에 객체 프로퍼티에 함수를 할당한다.
- 그렇다면 객체 **user**의 `hello`가 함수를 갖는 프로퍼티가 된다.
- 객체 내의 Method를 호출할 때는 `object.key()`로 호출한다.

```javascript
var user = {
  name : 'kim',
  age : 25,
}

user.hello = function() {
  console.log('hello')
}

user.hello()
```



- 이미 생성된 함수를 프로퍼티에 할당할 수도 있다.

```javascript
var user = {
  name : 'kim',
  age : 25,
}

function hello() {
  console.log('hello')
}

user.hello = hello
user.hello()
```



- 객체 리터럴 안에 Method를 선언할 수도 있다.

```javascript
var user = {
  name : 'kim',
  age : 25,
  hello(){
    console.log('hello')
  }
}

user.hello()
```



### 'this'

- 객체 내의 Method는 객체의 프로퍼티에 접근할 수 있어야한다. 이때 `this`를 사용하여 객체 내부의 프로퍼티에 접근할 수 있다.
- 아래의 코드를 보면 `hello()`에서 `this.name`을 사용하였다. `this`는 객체 자신을 가리킨다. 즉 `this.name`과 `user.name`은 같은 의미이다.

```javascript
var user = {
  name:'kim',
  age:25,
  hello(){
    console.log('hello')
    console.log(this.name)
  }
}

user.hello()
// hello
// kim
```



- Method 내에서 사용하는 `this`는 호출되는 객체에 따라 참조하는 값이 달라진다.

```javascript
var user1 ={
  name:'kim',
}

var user2={
  name:'lee',
}

function hello(){
  console.log(this.name,'hello')
}

user1.func=hello
user2.func=hello

user1.func() // kim hello가 출력된다.
user2.func() // lee hello가 출력된다.
```

