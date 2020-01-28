# How to setup typescript using three different approaches

## Using tsc (basic approach)

[See how to setup Webpack with Babel here](/snippets/frontend_webpack_babel.md)

### Setting up tsc

```yarn add --dev typescript```

```
project root
	+ tsconfig.json
```

```javascript
/* tsconfig.json */

{
	"compilerOptions": {
		"target": "ES5",	//Specify ECMAScript target version
		"module": "UMD",	//Specify module code generation
		"strict": true,		//Enable all strict type checking options
		"sourceMap": true,	//Generates corresponding .map file
		"declaration": true,	//Generates corresponding .d.ts file
		"outDir": "./build"	//Redirect output structure to the directory
	},
	"include": ["**/*.ts"],
	"exclude": ["node_modules"]
}
```

### Using AMD/UMD on frontend (requirejs)

```html
<script data-main="./index.js" src="./require.js"></script>
```

```javascript
export = {
	/*...module content*/
};
```

### Building app

```javascript
/* package.json */

{
	/* ... */
	"scripts": {
		"build": "tsc"
	}
	/* ... */
}
```

------------

## Using Webpack

```yarn add --dev typescript```

```yarn add --dev awesome-typescript-loader``` *- typescript loader for webpack*

```javascript
/* webpack.config.js */

module.exports = {
  /*...*/
  module: {
    rules: [
      {
        test: /\.(ts)$/,
        exclude: /node_modules/,
        loader: 'awesome-typescript-loader'
      }
    ]
  },
  resolve: {
    extensions: ['*', '.ts']
  }
  /*...*/
}
```

------------

## Using Babel preset

```yarn add --dev typescript```

```yarn add --dev @babel/preset-typescript``` *- typescript preset for babel*

```javascript
/* .babelrc */

{
  "presets": ["@babel/preset-typescript"]
}
```
