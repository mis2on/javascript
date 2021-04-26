# Hello, world!

## &lt;script&gt; 태그

&lt;script&gt;&lt;/script&gt; 태그를 이용해 html문서 안에 삽입할 수 있다.

· script 태그 type 속성 : type="text/javascript" 필수가 아님 

```javascript
<script type="text/javascript"></sciprt>
```

  
· script 태그 language 속성 : 현재 사용x, 필수가 아님 

· script 태그 src 속성 : 외부 스크립트 파일을 불러올 때 파일위치 경로 적는다. 절대경로와 상대경로 혹은 url 전체를 속성으로 사용할 수 있다. 

```javascript
<script src="js/script.js"></script>
```

src 속성이 있으면 태그 내부에 코드들은 실행되지 않기 때문에 따 분리해 작성해야 한다.

```javascript
<script src="js/script.js"></script>
<script>
    alert(1);
</script>
```

