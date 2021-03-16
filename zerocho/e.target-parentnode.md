# e.target과 parentNode

## e.target === 클릭된 애

클릭한 칸 td는 e.target

![](../.gitbook/assets/image%20%2830%29.png)

## e.target.parentNode === 클릭된 애 부모 태그

클릭한 td의 부모 tr은 e.target.parentNode

![](../.gitbook/assets/image%20%2829%29.png)

그렇다면 table 전체는?? e.target.parentNode.parentNode  
자식은? e.target.children

