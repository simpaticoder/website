

Make a staircase. Hardest part was losing the initial space with shift.
```js
function staircase(n) {
    const result = [];
    let level;
    for (let i = 0; i < n; i++){
        level = [];
        result.push(level);
        for (let j = 0; j <= n; j++){
            level.push((j < n - i) ? ' ' : '#');
        }
        level.shift();
    }
    const out = result.map(level => level.join('')).join('\n');
    console.log(out);
}
```


```js
function miniMaxSum(arr) {
    const sum = arr.reduce((a,b) => a+b);
    const s = arr.map(a => sum - a);
    s.sort();
    console.log(s.shift() + ' ' + s.pop());
}

```