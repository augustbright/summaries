# i18next (react-i18next) with NextJS

-----------------------------------------

## Setting up

1. ```npm i --save i18next react-i18next next-i18next```

Types not needed

2. No edits in **next.config.js**

3. Create **i18n.ts** in your **lib** folder

```javascript
/* lib/i18n.ts */

import NextI18Next from 'next-i18next';

const NextI18NextInstance = new NextI18Next({
    browserLanguageDetection: false,
    serverLanguageDetection: false,
    defaultLanguage: 'en',    
    defaultNS: 'translation',
    localePath: 'client/public/locales',
    otherLanguages: ['ru', 'en']
});

export default NextI18NextInstance;

export const {
    appWithTranslation,
    useTranslation,
    withTranslation,
    i18n
} = NextI18NextInstance;
```

4. Set up middleware (the default export) on express:

```javascript
/* server.ts */

/* ... */

    // Set up server i18n
    await nextI18NextInstance.initPromise;
    expressApp.use(nextI18NextMiddleware(nextI18NextInstance));

/* ... */
```

## Using

use:
    HOC: **withTranslation**
    HOOK: **useTranslation**
    Render prop: **Translation**
    Component: **Trans** 

```javascript
/* import interface and HOC */
import { WithTranslation } from "next-i18next";
import { withTranslation } from "../../lib/i18n";
```

```javascript

/* extend WithTranslation interface to get props */

interface IMyComponentProps extends WithTranslation {
}


/* use HOC */

export default withTranslation()(
    class MyComponent extends React.Component<IMyComponentProps> {
        render() {
            const {t, i18n} = this.props;

            /* use t() and i18n */
        }
    }
);

```

## Hacks

Because the "public" directory is different for server and client:
```javascript
    // A fix for next-i18next lang resolving
    expressApp.use('/client/public/', express.static(path.join(__dirname, '../client/public/')));
```


Because next-i18next is not working with cookies for some reason...
```javascript
    // Cookies
    expressApp.use(cookieParser());

    expressApp.use(async (req, res, next) => {
        const lang = req.cookies['next-i18next'] || 'en';
        await req.i18n.changeLanguage(lang);
        next();
    });

```