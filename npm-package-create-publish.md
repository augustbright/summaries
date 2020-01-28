# NPM Package: Creating & Publishing

--------------------------------------
[example](http://https://github.com/augustbright/react-scrollable "example")

## Building source code

1. Create project structure, init a new package, install webpack, babel, typescript dependencies
2. Install project dependencies, dev dependencies, peer dependencies
3. Configure webpack to build a library:

```javascript
/* webpack.config.js */

module.exports = {
    /* ... */
    output: {
        /* ... */

        /* this means, we want to build a library */
        library: 'reactScrollable',

        /* this is needed to correctly require peer dependencies, such as react */
        libraryTarget: 'umd'
    },

    /* ... */

    // Deps, not to be included into bundle
    externals: {
        react: {
            root: 'React',  // Script variable name
            commonjs: 'react',  // Commonjs module name
            commonjs2: 'react', // Commonjs module name
            amd: 'react'    // AMD module name
        }
    },

    /* ... */
}
```

4. Specify Babel's *@babel/preset-env* build target, e.g. current

```javascript
/* .babelrc */

    /* ... */

    ["@babel/preset-env", {
        "targets": {
            "node": "current"
        }
    }]

    /* ... */
```

5. Create **.npmignore**

6. Add **scripts** and **main** to **package.json**

```javascript
/* package.json */

{
  /* ... */

  "main": "dist/index.js",
  
  /* ... */

  "scripts": {
    "clean": "rm -rf dist",
    "build:src": "webpack --config webpack.config.js --mode production",
  },

  /* ... */
}
```

## Building declaration files

7. Configure typesctipt to build declarations (emitDeclarationOnly):

```javascript
/* tsconfig.json */

{
    "include": ["src/**/*"],
    "exclude": ["node_modules"],
    "compilerOptions": {
        "esModuleInterop": true,
        "emitDeclarationOnly": true,
        "declaration": true,
        "jsx": "react",
        "outDir": "dist"
    }
}

```

8. Add **scripts** and **types** to **package.json**

```javascript
/* package.json */

{
  /* ... */

  "types": "dist/index.d.js",
  
  /* ... */

  "scripts": {
    "clean": "rm -rf dist",
    "build": "npm run clean && npm run build:src && npm run build:declaration",
    "build:src": "webpack --config webpack.config.js --mode production",
    "build:declaration": "tsc"
  },

  /* ... */
}
```

## Checking & publishing

```npm pack``` - to check packing before publishing

```npm publish``` - to publish package to npmjs

Optionally, create **Github action** to automatically publish.
