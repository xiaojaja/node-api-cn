<!-- YAML
added: v8.0.0
changes:
  - version: v9.3.0
    pr-url: https://github.com/nodejs/node/pull/17152
    description: "`console.dirxml` now calls `console.log` for its arguments."
-->
* `...data` {any}

此方法调用 `console.log()` 将接收到的参数传递给它。 
此方法不会生成任何 XML 格式。

