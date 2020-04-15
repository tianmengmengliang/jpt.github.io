JS判断值是否是数字
```markdown
    // isNaN()函数 把空串 空格 以及NUll 按照0来处理 所以用typeof先去除，
    // typeof判断 NaN 竟然是number类型。

    function myIsNaN(value) {
        return typeof value === ‘number‘ && !isNaN(value);
    }
```
