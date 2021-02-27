# codeup

> codeup의 기초 100제를 자바스크립트로 풀면서 문법에 익숙해지기



### 정수 1개 입력받아 카운트다운 출력하기

- `while`문으로 100부터 1까지 출력하기

```javascript
var count = 100;
while(count > 0){
  console.log(count);
  count--;
}
```



### 1~100까지 짝수의 합 구하기

```javascript
var sum = 0;
for(var i=1; i<101; i++){
  if(i%2==0){
    sum += i;
  }
}
console.log(sum)
```



### 3 6 9 게임

- 3, 6, 9가 들어갔을 때 X 출력하기
- 1부터 100까지 3, 6, 9가 들어가면 X를 출력하고 아니면 숫자를 출력하기

```javascript
for(var i=1; i<100; i++){
  var num = String(i)
  var word = ''
  var flag = false
  for(var j=0; j<num.length; j++){
    if(num[j]=='3' || num[j]=='6' || num[j]=='9'){
      flag = true
      word += 'X'
    }
  }
  if(flag){
    console.log(word)
  }
  else{
    console.log(num)
  }
}
```



### 3의 배수는 통과

- 1부터 100까지의 숫자 중에 3의 배수빼고 모두 출력하기

```javascript
for(var i=1; i<101; i++){
  if(i%3==0){
    continue;
  }
  else{
    console.log(i);
  }
}
```



### 등차수열

- 1부터 시작하여 n만큼 커지는 등차수열이 있을 때 10번째 숫자 출력하기

```javascript
var number = 1;
var n = 3;
for(var i=0; i<10; i++){
  number += n;
}
console.log(number);
```



### 배열 거꾸로 출력하기

- 배열에 포함된 숫자를 `for`문으로 거꾸로 출력하기

```javascript
var arr = [1, 2, 3, 4, 5]
for(var i=arr.length-1; i>=0; i--){
  console.log(arr[i])
}
```



### 