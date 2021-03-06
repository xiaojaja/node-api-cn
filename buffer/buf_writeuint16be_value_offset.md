<!-- YAML
added: v0.5.5
changes:
  - version: v10.0.0
    pr-url: https://github.com/nodejs/node/pull/18395
    description: Removed `noAssert` and no implicit coercion of the offset
                 to `uint32` anymore.
-->

* `value` {integer} 要写入 `buf` 的数值。
* `offset` {integer} 开始写入之前要跳过的字节数。必须满足：`0 <= offset <= buf.length - 2`。**默认值:** `0`。
* 返回: {integer} `offset` 加上已写入的字节数。

将 `value` 作为大端序写入到 `buf` 中指定的 `offset` 位置。
`value` 必须是无符号的 16 位整数。
当 `value` 不是无符号的 16 位整数时，行为是未定义的。

```js
const buf = Buffer.allocUnsafe(4);

buf.writeUInt16BE(0xdead, 0);
buf.writeUInt16BE(0xbeef, 2);

console.log(buf);
// 打印: <Buffer de ad be ef>
```

