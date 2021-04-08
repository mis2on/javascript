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

//규칙찾아보기console.log(' '.repeat(n+3) + '*'.repeat(n))
console.log(' '.repeat(n+2) + '*'.repeat(n+1))
console.log(' '.repeat(n+1) + '*'.repeat(n+2))
console.log(' '.repeat(n) + '*'.repeat(n+3))
console.log(' '.repeat(0) + '*'.repeat(n+4))


```

★ 규칙을 잘 파악하자

