# Using React Router

1. Install react-router-dom dependency for browser usage:

```yarn add react-router-dom```

2. Configure webpack-dev-server to fallback to index page instead of 404:

```javascript
/* webpack.config.js */

{
	/* ... */
	devServer: {
		/* ... */
		historyApiFallback: true
	}
	/* ... */
}
```

3. Wrap your application with **BrowserRouter**:

```
class App extends Component {
	render() {
		<BrowserRouter>
			...
		</BrowserRouter>
	}
}
```

4. Use **Switch** and **Route** to handle routing:

```
...
<Switch>
	<Route exact path="/" component={Home}/>
	<Route path="/about" component={About}/>
	<Route path="/item/:id" component={Item}/>
</Switch>
...
```

5. For dynamic routing the components are given extra props: **history**, **location** and **match**:

```javascript
{
   "history": {
      "length": 12,
      "action": "POP",
      "location": {
         "pathname": "/item/101",
         "search": "",
         "hash": ""
      }
   },
   "location": {
      "pathname": "/item/101",
      "search": "",
      "hash": ""
   },
   "match": {
      "path": "/item/:id",
      "url": "/item/101",
      "isExact": true,
      "params": {
         "id": "101"
      }
   }
}
```
