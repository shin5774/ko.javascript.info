# setTimeout에서의 에러

`.catch`가 트리거가 된다고 생각하시나요? 답을 설명해주세요.

```js
new Promise(function(resolve, reject) {
  setTimeout(() => {
    throw new Error("에러 발생!");
  }, 1000);
}).catch(alert);
```
