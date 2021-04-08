# 반복문사용 & 별찍기

```javascript
console.log('*'.repeat(1))
console.log('*'.repeat(2))
console.log('*'.repeat(3))
console.log('*'.repeat(4))
console.log('*'.repeat(5))

*
**
***
****
*****
```

```javascript
let n = 1
while(n <= 5) {
    console.log('*'.repeat(n))
    n = n + 1
}
```

## 

```javascript
console.log('*'.repeat(5))
console.log('*'.repeat(4))
console.log('*'.repeat(3))
console.log('*'.repeat(2))
console.log('*'.repeat(1))

*****
****
***
**
*
```

```javascript
let n = 5
while(n >= 1) {
    console.log('*'.repeat(n))
    n = n - 1
}
```

## 

```javascript
console.log('    *')
console.log('   **')
console.log('  ***')
console.log(' ****')
console.log('*****')

console.log(' '.repeat(4) + '*'.repeat(1))
console.log(' '.repeat(3) + '*'.repeat(2))
console.log(' '.repeat(2) + '*'.repeat(3))
console.log(' '.repeat(1) + '*'.repeat(4))
console.log(' '.repeat(0) + '*'.repeat(5))

    *
   **
  ***
 ****
*****

//규칙찾아보기
console.log(' '.repeat(5-n) + '*'.repeat(n))
```

```javascript
let n = 1;
while(n <= 5) {
    console.log(' '.repeat(5-n) + '*'.repeat(n))
    n = n + 1    // n += 1,    n++
}
```

★ 규칙을 잘 파악하자!

무한반복 매크로를 멈추고 싶을 때 shift + ESC 눌러 크롬만의 작업관리자에 끄기

