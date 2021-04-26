---
description: 브라우저는 사용자와 상호작용할 수 있는 세가지 함수를 제공한다.
---

# alert, prompt, confirm을 이용한 상호작용

## alert

사용자가 확인버튼을 누를 때까지 메세지를 보여주는 창이 계속 떠있는다.

```javascript
alert("Hello!");
```

메세지가 있는 작은 창을 모달창이라고 부른다.

![](../.gitbook/assets/image%20%2842%29.png)

## prompt

두 개의 인수를 받는다. 함수가 실행되면 텍스트 메세지와 입력필드, 확인 및 취소 버튼이 있는 모달창을 띄워준다.

```javascript
result = prompt(title, [default]);
//title 사용자에게 보여줄 문자열
//[default] 입력 필드의 초깃값
```

![](../.gitbook/assets/image%20%2846%29.png)

![](../.gitbook/assets/image%20%2844%29.png)

## confirm 대화상자

매개변수로 받은 question\(질문\)과 확인 및 취소 버튼이 있는 모달창을 보여준다.  
사용자가 확인버튼을 누르면 true, 그 외의 경우는 false를 반환

```javascript
result = confirm(question);
```

```javascript
let isBoss = confirm("당신이 주인인가요?");
alert(isBoss);    //확인 버튼을 눌렀다면 ture가 출력된다.
```

![](../.gitbook/assets/image%20%2847%29.png)

확인버튼을 눌렀을 때

![](../.gitbook/assets/image%20%2845%29.png)

취소버튼을 눌렀을 때

![](../.gitbook/assets/image%20%2843%29.png)

