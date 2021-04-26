# 논리 연산자

 \|\|\(OR\), &&\(AND\), !\(NOT\) 논리 연산가 있다.

## \|\|\(OR\)

인수 중 하나라도 true 이면 true를 반환하고, 그렇지 않으면 false를 반환한다.

```javascript
alert(true || true); //true
alert(false || true); //true
alert(true || false); //true
alert(false || false); //false
```

피연산자가 모두 false인 경우를 제외하고 연산 결과는 항상 true  
숫자1은 true, 숫자0은 false로 바뀐다.

## &&\(AND\)

두 피연산자가 모두가 참일때 true를 반환하고 그 외에는 false를 반환한다.

```javascript
alert(true && true); //true
alert(false && true); //false
alert(true && false); //false
alert(false && false); //false
```

AND 연산자 &&의 우선순위는 OR 연산자 \|\| 보다 높습니다.

## !\(NOT\)

NOT 연산자의 우선순위는 모든 논리 연산자 중에서 가장 높기 때문에 항상 && 나 \|\| 보다 먼저 실행된다.

