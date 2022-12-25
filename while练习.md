# 1.假设银行存款年利率为5%，问1000元存多少年可以变成5000
## 答1：
```js
let rate = 0.05;
let asset = 1000;
let year = 0;
while (true) {
    currentAsset = asset * rate + asset
    asset = currentAsset
    year++
    if (currentAsset >= 5000) {
        alert(`一共需要存${year}年，所有存款为${asset}元`)
        break
    }
}

```
## 答2:
```js
let asset = 1000;
let year = 0;
while (asset < 5000) {
    asset *= 1.05
    year++
}
alert(`一共需要存${year}年，所有存款为${asset}元`)
```
