# AMD, CommonJS, UMD

## AMD - Asynchronous Module Definition (RequireJS)

**Definition**:
```javascript
/* foo.js */
define([/* ...dependencies */], function ($) {
    return {
		/* module definition */
	};
});
```

**Imports**:
```javascript
/* Using Requirejs */
require(['./foo.js'], (foo) => {
	/* foo is available here */
});
```

## CommonJS (Node.js)

**Definition**:
```javascript
/* foo.js */

export const a = 1;
export default func = () => {};
```

**Imports**:
```javascript
import func from './foo';
import { a } from './foo';
import { a as myConst } from './foo';
import * as foo from './foo';
```

## UMD - Universal Module Definition (RequireJS + Node.js)

**Definition**:
```javascript
(function (root, factory) {
    if (typeof define === 'function' && define.amd) {
        // AMD
        define(['jquery'], factory);
    } else if (typeof exports === 'object') {
        // Node, CommonJS-like
        module.exports = factory(require('jquery'));
    } else {
        // Browser globals (root is window)
        root.returnExports = factory(root.jQuery);
    }
}(this, function ($) {
    //    methods
    function myFunc(){};

    //    exposed public method
    return myFunc;
}));
```
