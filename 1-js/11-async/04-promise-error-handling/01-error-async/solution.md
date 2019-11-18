정답은 **아니, 그렇지 않다** 입니다.

```js run
new Promise(function(resolve, reject) {
  setTimeout(() => {
    throw new Error("에러 발생!");
  }, 1000);
}).catch(alert);
```

이 장에서 언급했듯이, 함수 코드에는 '암시적 `try..catch`'가 있습니다. 따라서 모든 동기 에러가 처리됩니다.

하지만 여기에서 에러는 executor(실행자, 실행 함수)가 실행되는 동안이 아니라 나중에 발생합니다. 따라서 프라미스는 에러를 처리할 수 없습니다. 
