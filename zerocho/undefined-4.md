# 별찍기\(반복문 연습\)

## 별 더하기

```javascript
for(var star = 1; star <= 5; star += 1) {
    console.log('*'.repeat(star))
}

//결과값
*
**
***
****
*****
```

star += 1  
star = star + 1

## 별 빼기

```javascript
for(var star = 5; star >= 1; star -= 1) {
    console.log('*'.repeat(star))
}

//결과값
*****
****
***
**
*
```

star -= 1  
star = star - 1

## 문제1

```javascript
**********    //10개
********      // 8개
******        // 6개
****          // 4개
**            // 2개

for(var star = 10; star >= 2; star -= 2) {
    console.log('*'.repeat(star))
}
```

## 문제2

```javascript
*                   // 1     
**                  // 2개    
****                // 4개    
********            // 8개
****************    //16개

for(var star = 1; star <= 16; star *= 2) {
    console.log('*'.repeat(star))
}

star
32
```

## 문제3

```javascript
*****
 ****
  ***
   **
    *
    
for(var star = 5; star >= 1; star -= 1) {
    console.log(' '.repeat(5 - star) + '*'.repeat(star))
    
}
```

규칙을 찾는게 중요!  
\*은 하나씩 줄어들고,  
공백은 하나씩 늘어나고

' ' + '\*' === ' \*'  

## 문제4

```javascript
*********
 *******
  *****
   ***
    *
    
for(var star = 9; star >= 1; star -= 2) {
    console.log(' '.repeat((9 - star)/2) + '*'.repeat(star))
    
} 
```

규칙을 찾는게 중요!  
\*은 하나씩 줄어들고,  
공백은 하나씩 늘어나고

' ' + '\*' === ' \*'  

