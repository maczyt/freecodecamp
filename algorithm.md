1. 反转字符串

``` js
const reverse = (str) => str.split('').reverse().join('')
```

2. Factorialize a Number(阶乘)

``` js
const factorialize = (num) => { if (num === 0) return 1; return num * factorialize(num - 1); }
```

3. Check for Palindromes(回文)

```js
const palindrome = (str) => {
  const removeReg = /[^0-9a-zA-Z]/g;
  str = str.replace(removeReg, '').toLowerCase();
  return str === str.split('').reverse().join('');
}
```

4. Find the Longest Word in a String

```js
const findLongestWord = (str) => {
  return str.split(' ').reduce((a, b) => { if (a.length > b.length) { return a; }  return b; }, '').length
}
```

5. Title Case a Sentence

```js
const titleCase = (str) => {
  return str.toLowerCase().split(' ')
    .map(s => s.slice(0, 1).toUpperCase() + s.slice(1); }).join(' ')
}
```

6. Return Largest Numbers in Arrays

```js
const largestOfFour = (arr) => {
  return arr.map(item => item.reduce((a, b) => { if (a > b) { return a; } return b; }, 0))
}
```

7. Confirm the Ending

``` js
const confirmEnding = (str, target) => {
  return str.substr(str.length - target.length, target.length) === target
}
```

8. Repeat a string repeat a string

```js
const repeatStringNumTimes = (str, num) => {
  return str.repeat(num)
}
```

9. Truncate a string

```js
const truncateString = (str, num) => {
  if (num >= str.length) return str;
  if (num > 3) return str.substr(0, num - 3) + '...'
  return str.substr(0, num) + '...'
}
```

10. Chunky Monkey

```js
const chunkArrayInGroups = (arr, size) => {
  let res = []
  arr = arr.slice()
  while (arr.length > 0) {
    res.push(arr.splice(0, size))
  }
  return res
}
```