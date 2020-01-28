# Advanced styling with SASS
1. [Setup styling loaders for your Webpack application](./webpack-styling.md)

2. Install dependencies for SASS:

* ```yarn add node-sass``` *- The SASS converter for Node.js*
* ```yarn add sass-loader``` *- SASS loader for webpack*

2. Configure Webpack to use loaders for SASS files:

```javascript
/* webpack.config.js */

module.exports = {
	/* ... */
	module: {
		rules: [
			/* ... */
			{ test: /\.s[ac]ss$/, exclude: /node_modules/, use: ['style-loader', 'css-loader', 'sass-loader'] }
		]
	}
	/* ... */
};
```

3. Now you can import .sass and .scss files from your code:

```css
// const.scss
$bg_color: green;
```

```css
// style.scss
@import './const.scss';

body {
	background: $bg_color;
}
```

```javascript
/* index.js */

import './style/style.scss';
```
