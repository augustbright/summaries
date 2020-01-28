# React API

* [Importing](#importing)
* [Components](#components)
* [Lifecycle methods](#component-lifycycle-methods)
* [Elements](#elements)
* [Children](#children)
* [Fragments](#fragments)
* [Refs](#refs)

## Importing

```javascript
import React from "react";
```

## Components
#### React.Component

```javascript
class MyComponent extends React.Component {
  render() {
    return <div />;
  }
}
```

#### React.PureComponent 

shalowly compares props & state in shouldComponentUpdate()

```javascript
class MyPureComponent extends React.PureComponent {
  render() {
    return <div />;
  }
}
```

#### Function components

```javascript
const MyFunctionComponent = props => {
  return <div />;
};
```

#### React.memo

Memo HOC - same as PureComponent, but for functional components:

```javascript
const MyMemoComponent = React.memo(MyFunctionComponent);
```

With custom prop comparison:

```javascript
const MyMemoComponentWithCustomCheck = React.memo(
  MyFunctionComponent,
  (prevProps, nextProps) => {
    // here compare prevProps with nextProps
    return true;
  }
);
```

## Component lifecycle methods
#### Common methods

* constructor(props)
* componentDidMount()
* componentDidUpdate(prevState, prevProps, snapshot)
* ComponentWillUnmount()

#### Rarely used lifecycle methods

* shouldComponentUpdate(nextProps, nextState): Boolean
* static getDerivedStateFromProps(props, state): Object
* getSnapshotBeforeUpdate(prevProps, prevState): any or null

#### Error boundaries

* static getDerivedStateFromError(error): Object
* componentDidCatch(error, info)

#### Legacy lifecycle methods

* UNSAFE_componentWillMount()
* UNSAFE_componentWillReceiveProps()
* UNSAFE_componentWillUpdate(nextProps, nextState)

## Elements
The following methods are typically called indirectly with JSX.

#### Create element

```javascript
const myElement = React.createElement(
  MyComponent,	/* Component or tag */
  {
    /* props */
  } /* ...children */
);
```

#### Clone element

The clone preserves key & ref of the original

```javascript
const myClonedElement = React.cloneElement(
  myElement,
  {
    /* shallow merged props */
  } /* ...replaceChildren */
);
```

#### Validate element

```javascript
React.isValidElement(myElement); // true
```

## Children

The following methods take **props.children** as an argument.

#### Mapping

```javascript
const childrenMapped = React.Children.map(
  props.children,
  (child, index) => null /* return anything */
);
```

#### Iterating

```javascript
React.Children.forEach(props.children, (child, index) => {});
```

#### Counting

```javascript
const childrenCount = React.Children.count(props.children);
```

#### Is only child

```javascript
const isOnlyChild = React.Children.only(props.children);
```

#### To array

```javascript
const childrenArray = React.Children.toArray(props.children);
```

## Fragments

```javascript
const myFragment = (
  <React.Fragment>
    Some text.
    <h2>Heading</h2>
    <div>Content</div>
  </React.Fragment>
);

const myShorthandFragment = (
  <>
    Some text.
    <h2>Heading</h2>
    <div>Content</div>
  </>
);
```

## Refs
#### Creating refs

```javascript
class MyComponentWithRef extends React.Component {
  constructor(props) {
    super(props);
    this.inputRef = React.createRef();
  }

  render() {
    return <input type="text" ref={this.inputRef} />;
  }

  componentDidMount() {
    this.inputRef.current.focus();
  }
}
```

#### Forwarding refs

```javascript
const FancyButton = React.forwardRef((props, ref) => (
  <button ref={ref} className="FancyButton">
    {props.children}
  </button>
));
const buttonRef = React.createRef();
<FancyButton ref={buttonRef}>Click me!</FancyButton>;
```
