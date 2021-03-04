# 산술연산자, 비교연산자

## 산술 연산자

{% tabs %}
{% tab title="+ 더하기" %}
1 + 2  
3
{% endtab %}

{% tab title="- 빼기" %}
3 - 2  
1
{% endtab %}

{% tab title="\* 곱하기" %}
12  \* 12  
144
{% endtab %}

{% tab title="/ 나누기" %}
144 / 12  
12
{% endtab %}

{% tab title="% 나머지" %}
12 % 11  
1
{% endtab %}
{% endtabs %}

## 비교 연산자

{% tabs %}
{% tab title=">, < " %}
5 &gt; 3  
true

5 &lt; 3  
false

'문자' &lt; 5  
false

5 &gt;= 5 크거나 같다  
ture

6 &lt;= 4 작거나 같다.  
false
{% endtab %}

{% tab title="==" %}
'문자' == '문자'  
true

false ==  false  
true

5 == 4  
false
{% endtab %}
{% endtabs %}

## ==과 === 비

```javascript
5 == '5' //true
NaN == NaN //false

★ 비교할때는 == 대신 === 사용해라!
5 == '5' //true
5 === '5' //false

★ !=, !== 부정
5 != '5' //false
5 !== '5' //true
```

## 비교 예외 NaN

NaN은 Not a Number  
NaN == NaN  
무조건 false

## 연산자 우선순위

사칙연산 =&gt; 부등호 =&gt; =이 제일 마지막에 실  
소괄호를 사용하면 연산자 우선수위를 바꿀 수 있다.  
더하기 연산자는 숫자뿐 아니라 문자도 합칠 수 있다.

```javascript
'문자1' + '문자2'
"문자1문자2"

'문자2' + 5
"문자25"    //문자열 뒤 숫자 문자로 취

'abc' + 'def'
"abcdef"

String(5)    //숫자를 문자로 바꿈
"5"

Number('5')    //문자를 숫자로 바꿈
5    
```



