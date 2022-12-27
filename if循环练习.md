# 1. 求1000以内的水仙花数
```js
for (i = 100; i <= 999; i++) {
    let hunds = parseInt(i / 100)
    let tens = parseInt((i - hunds * 100) / 10)
    let digit = parseFloat(i % 10)
    if (i === hunds ** 3 + tens ** 3 + digit ** 3) {
        var result = i
    }
    console.log(result);
}
```
