# Effect

Runs after the DOM is changed.

```javascript
useEffect(() => {
   // Update the document title using the browser API
   document.title = `You clicked ${count} times`;
});
```

### Triggers

The second argument defines the triggers:

```javascript
useEffect(() => {
   document.title = `You clicked ${count} times`;
}, [document]);
```

When empty it will only run when the component mounts or dismounts:

```javascript
useEffect(() => {
   document.title = `You clicked ${count} times`;
}, []);
```

## More Information

* [Using the Effect Hook](https://reactjs.org/docs/hooks-effect.html)

