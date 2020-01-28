# Creating serverless application with Webpack and Babel

--------------------------------------

## Project structure

```
+ project root
	+ dist
		+ index.html
	+ src
		+ index.js
```

*index.html:*
```html
<!doctype html>

<html lang="en">
	<head>
		<meta charset="utf-8">

		<title>PAGE TITLE</title>
		<meta name="description" content="PAGE DESCRIPTION">
		<meta name="author" content="PAGE AUTHOR">
	</head>

	<body>
		<div id="root"></div>
		<script src="./bundle.js"></script>
	</body>
</html>
```

-----------------------------

## Webpack setup
### Dependencies

```yarn add --dev webpack webpack-cli```

### Configuration

```
project root
	+  webpack.config.js
```

```javascript
/* webpack.config.js */

module.exports = {
	entry: './src/index.js',
	output: {
		path: __dirname + '/dist',
		publicPath: '/',
		filename: 'bundle.js'
	}
};
```

--------------------------------

### Building

```javascript
/* package.json */

{
	"scripts": {
		"build:dev": "webpack --config ./webpack.config.js --mode development",
		"build": "webpack --config ./webpack.config.js" --mode production
	}
}
```

### Dev serving & hot reload

```yarn add --dev webpack-dev-server```

```javascript
/* webpack.config.js */

module.exports = {
	/*...*/
	devServer: {
		contentBase: './build'
	},
	resolve: {
		extensions: ['*', '.js']
	}
};
```

```javascript
/* package.json */

{
	"scripts": {
		"dev": "webpack-dev-server --config ./webpack.config.js --mode development"
	}
}
```

### Static serving example

```yarn add --dev static-server```

```javascript
/* package.json */

{
	"scripts": {
		"start": "static-server ./build"
	}
}
```

--------------------------------------

## Babel setup

```yarn add --dev @babel/core @babel/preset-env``` *- Babel itself + modern features support*

```yarn add --dev babel-loader``` *- Babel loader for Webpack*

```
project root
	+ .babelrc
```

```javascript
/* .babelrc */

{
	"presets": [
		"@babel/preset-env"
	]
}
```

```javascript
/* webpack.config.js */

module.exports = {
	/*...*/
	module: {
		rules: [
			{
				test: /\.(js)$/,
				exclude: /node_modules/,
				use: ['babel-loader']
			}
		]
	},
	resolve: {
		extensions: ['*', '.js']
	},
	/*...*/
};
```
