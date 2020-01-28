# Styling Webpack application

1. Install dependencies:

* ```yarn add style-loader css-loader```

2. Configure Webpack to use loaders for css files:

```javascript
/* webpack.config.js */

module.exports = {
	/* ... */
	module: {
		rules: [
			/* ... */
			{ test: /\.css$/, exclude: /node_modules/, use: ['style-loader', 'css-loader'] }
		]
	}
	/* ... */
};
```

3. Now you can import css files from your code:

```css
// styles.css

body {
	background: green;
}
```

```javascript
/* index.js */

import './style/style.css';
```

By default, all styles will be inserted into a ```<style>``` tag.
