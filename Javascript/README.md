# Javascript 익히기

> - 웹 게임을 만들면서 Javascript 익히기
> - zerocho님의 강의를 기반으로



## Section00. 끝말잇기

- 브라우저에서 `prompt`와 `alert`를 지원해준다. 
- `prompt`는 사용자로부터 어떠한 값을 입력받으며 `alert`는 사용자에게 어떠한 알림을 출력하는 기능을 한다.

```javascript
var word = 'apple';
while(true){
  var new_word = prompt(word);
  if(word[word.length - 1] === new_word[0]){
    word = new_word;
  }
  else{
    alert("다시 입력하세요.")
  }
}
```

