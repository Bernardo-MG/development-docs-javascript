# PropTypes

Used to validate parameters.

```javascript
function SaveButton({ onClick }) {
   return <IconButton onClick={onClick}>
      <SaveIcon />
   </IconButton>;
}

SaveButton.propTypes = {
   onClick: PropTypes.func.isRequired
};
```

## Complex Types

```javascript
PropTypes.shape({
   text: PropTypes.string,
   link: PropTypes.string,
   id: PropTypes.string
})
```

## More Information

* [Typechecking With Proptypes](https://reactjs.org/docs/typechecking-with-proptypes.html)

