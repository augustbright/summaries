# Creating React application with Typescript without using create-react-app

**Step 1.** Create a new application.
1. [Setup Webpack and Babel](./modern-frontend.md)
2. [Setup Typescript](./typescript-setup.md)

----------------------

**Step 2.** Install dependencies for React:

* ```yarn add react react-dom``` - React library with dom-adapter.
* ```yarn add @babel/preset-react``` - React preset for Babel

-------------------

**Step 3.** Configure:

```javascript
/* .babelrc */

{
	"@babel/preset-react",
	["@babel/preset-typescript", {"isTSX": true, "allExtensions": true}]	// Configure preset-typescript to use .tsx
}
```

```javascript
/* .webpack.config.js */

module.exports = {
	/* ... */
	module: {
		rules: [
			/* ... */
			{ test: /\.tsx$/, exclude: /node_modules/, use: 'babel-loader' }
		]
	},
	resolve: {
		extensions: ['*', '.js', /* ... */, '.ts', '.tsx']
	}
	/* ... */
}
```

**Step 4.** Code:

* Create the main App component:

```javascript
/* ./src/App.tsx */

	import React from 'react';
	
	export default class App extends React.Component {
		render() {
			return (
				<div className="app">
					<h1>Greetings!</h1>
					<p>This is a React application.</p>
				</div>
			);
		}
	}
```

* Create entry file for your application:

```javascript
/* ./src/index.tsx */

import React from 'react';
import ReactDOM from 'react-dom';
import App from './src/App';

ReactDOM.render(<App/>, document.getElementById('root'));
```
