那是因为 `i` 永远不会等于 `10`。

运行下面这段代码来查看 `i` 的 **实际** 值：

```js run
let i = 0;
while (i < 11) {
  i += 0.2;
  if (i > 9.8 && i < 10.2) alert( i );
}
```

它们中没有一个恰好是 `10`。

之所以发生这种情况，是因为对 `0.2` 这样的小数时进行加法运算时出现了精度损失。

结论：在处理小数时避免相等性检查。
