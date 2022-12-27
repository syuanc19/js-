# 1. 求1000以内的水仙花数
```js
for (i = 100; i <= 999; i++) {
    let hunds = parseInt(i / 100) // 把(i/100)套用parseInt，得到百位数
    let tens = parseInt((i - hunds * 100) / 10) // i-hunds*100会得到两位数，再除以10后套用parseInt则能获得十位数
    let digit = parseInt(i % 10) // i幂10直接获得余数(也就是个位数)
    if (i === hunds ** 3 + tens ** 3 + digit ** 3) {
        console.log(i);
    }
}
```
## 索引写法
```js
        for (i = 100; i <= 999; i++) {
            let strI = i + '' //让i转成字符串
            if (strI[0] ** 3 + strI[1] ** 3 + strI[2] ** 3 === i) { //判断i的第一、第二，第三位数的三次幂，是否等于i
                console.log(i)
            }
        }
```
***
# 2. 获取用户输入的大于1的整数(不考虑输错)，检查该数字是否为质数，并打印结果
```js
        let result = +prompt('请输入大于1的整数');
        let count = true; // 这里假设该数本身就是质数
        for (i = 2; i < result; i++) {
            if (result % i === 0) {  // 该if函数说明如果我们输入的数字 % i后等于0，代表i到我们的数字之间有该数的因数，因此让count变为false
                count = false
            }
        }
        if (count === true) {
            alert(`${result}是质数`)
        } else if (count === false) {
            alert(`${result}不是质数`)
        }
```
