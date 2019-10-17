# Redux for React

## Using HoC

```javascript
function SearchView({ action }) {
   // The rest of the code
   return ...
}

const mapStateToProps = (state) => {
   return {
      loading: selectSearchingBooks(state)
   };
};

const mapDispatchToProps = (dispatch) => {
   return {
      action: bindActionCreators(search, dispatch)
   };
};

export default connect(
   mapStateToProps,
   mapDispatchToProps
)(SearchView);
```

## Using Hooks

```javascript
function SearchView() {
   const loading = useSelector(selectSearchingBooks);

   const dispatch = useDispatch();
   const action = () => dispatch(search());

   // The rest of the code
   return ...
}

export default SearchView;
```

