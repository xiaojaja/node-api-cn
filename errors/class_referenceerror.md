
* 继承自: {errors.Error}

表明试图访问一个未定义的变量。
此类错误通常表明代码有拼写错误或程序已损坏。

虽然客户端代码可能产生和传播这些错误，但在实践中，只有 V8 引擎会这么做。

```js
doesNotExist;
// 抛出 ReferenceError，在这个程序中 doesNotExist 不是一个变量。
```

除非应用程序是动态地生成并运行代码，否则 `ReferenceError` 实例表示代码中或其依赖中的错误。

