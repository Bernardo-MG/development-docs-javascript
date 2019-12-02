# Destructuring

## Assignment

```javascript
[a, b, ...rest] = [10, 20, 30, 40, 50];

console.log(a);
// expected output: 10

console.log(b);
// expected output: 20

console.log(rest);
// expected output: [30,40,50]
```

## Function Params

```javascript
function someFunction({ a, b, ...rest })
```

## More Information

* [Destructuring Assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)

