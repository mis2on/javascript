# null, undefined

## 변수 생성, 변수값 변

```javascript
var empty    //empty라는 변수를 만들고 값을 넣지 않음
empty
undefined    //일종의 값
var empty = 5    //undefined
empty
5    //변수가 기억하고 있는 값을 바꿀 수 있다.
```

```javascript
var name = '몽실'
name
'몽실'
name = '구름'    //name 변수값을 구름으로 변경
name
'구름'
name = undefined    //name 변수값을 삭제
name
undefined
```

앞에 var 붙어 있으면 변수를 새로 만드는것  
var이 붙어 있지 않으면 값을 바꾸는 것 

## undefined와 null

**undefined** 변수를 만들고 아무것도 넣지 않았을 때 컴퓨터가 기본으로 넣어준 값  
**null**은 내가 넣어준 빈    
  
원래 값이 있다가 지우고자 할  undefined보다 null을 사용하면   
컴퓨터가 넣은 값과 내가 넣은 값을 구별할 수 있다. 

undefind 보다 **null** 쓰는 게  좋다.

