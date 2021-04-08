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

