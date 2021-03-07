# 끝말잇기 구현

![&#xBC18;&#xBCF5;&#xBB38;&#xC740; &#xC21C;&#xC11C;&#xB3C4;&#xB97C; &#xADF8;&#xB824;&#xBCF4;&#xBA74; &#xC88B;&#xB2E4;](../.gitbook/assets/image%20%288%29.png)

## while문 사용하여 끝말잇기 구

```javascript
var word = '몽실';
while(true) {
    var newword = prompt(word);
    if(word[word.length -1] === newword[0]) {
        word = newword;
    } else {
        alert('끝말잇기란 말이에오!')
    }
}
```

![](../.gitbook/assets/image%20%2811%29.png)

![](../.gitbook/assets/image%20%2810%29.png)

![](../.gitbook/assets/image%20%287%29.png)

![](../.gitbook/assets/image%20%2812%29.png)

alert, prompt, console.log 는 브라우저가 만들어준 함수이다.  
따라서 따로 함수정의 할 필요가 없다.

