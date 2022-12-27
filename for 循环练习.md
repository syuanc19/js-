# 1. 求1000以内的水仙花数
```js
for (i = 100; i <= 999; i++) {
    let hunds = parseInt(i / 100)
    let tens = parseInt((i - hunds * 100) / 10)
    let digit = parseFloat(i % 10)
    if (i === hunds ** 3 + tens ** 3 + digit ** 3) {
        console.log(result);
    }
}
```
## 索引写法
```js
        for (i = 100; i <= 999; i++) {
            let strI = i + ''
            if (strI[0] ** 3 + strI[1] ** 3 + strI[2] ** 3 === i) {
                console.log(i)
            }
        }
```
# 2. 获取用户输入的大于1的整数(不考虑输错)，检查该数字是否为质数，并打印结果
```js
        let result = +prompt('请输入大于1的整数');
        let count = true;
        for (i = 2; i < result; i++) {
            if (result % i === 0) {
                count = false
            }
        }
        if (count === true) {
            alert(`${result}是质数`)
        } else if (count === false) {
            alert(`${result}不是质数`)
        }
```
