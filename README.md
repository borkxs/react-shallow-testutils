# react-shallow-testutils
Replacement for TestUtils when using React's shallow rendering.

[![Circle CI](https://circleci.com/gh/sheepsteak/react-shallow-testutils.png?circle-token=acb1a68cfaeb110ccc4901ac8171750fcbadf5b5)](https://circleci.com/gh/sheepsteak/react-shallow-testutils)

```
npm install react-shallow-testutils
```

### Renderer
A wrapper around React's [shallow rendering](http://facebook.github.io/react/docs/test-utils.html#shallow-rendering) that makes it easier to use a context.

```javascript
this.renderer = new Renderer();
const componentTree = this.renderer.render(function componentClass, Object context, Object props);
```

### isComponentOfType
Returns whether a component instance is of a particular type.

```javascript
boolean isComponentOfType(ReactComponent component, function componentClass)
```

### isDOMComponent
Returns whether the supplied component is a DOM component or not

```javascript
boolean isDOMComponent(function component)
```

### findAll

Traverses the component tree and returns the components that satisfy the supplied function.

```javascript
array findAll(ReactComponent tree, function test)
```

### findAllWithType
Similar to [scryRenderedComponentsWithType](http://facebook.github.io/react/docs/test-utils.html#scryrenderedcomponentswithtype), finds all components in the tree that match a certain type or DOM tag.

```javascript
array findAllWithType(ReactComponent tree, function componentClass | string tagName)
```

### findWithType
Similar to [findRenderedComponentWithType](http://facebook.github.io/react/docs/test-utils.html#findrenderedcomponentwithtype), find one component in the tree that matches a certain type or DOM tag. If none or more than one then throws an error.

```javascript
ReactComponent findAllType(ReactComponent tree, function componentClass | string tagName)
```

### findAllWithClass
Similar to [scryRenderedDOMComponentsWithClass](http://facebook.github.io/react/docs/test-utils.html#scryRenderedDOMComponentsWithClass), finds all components in the tree that match a certain class name.

```javascript
array findAllWithClass(ReactComponent tree, string className)
```

### findWithClass
Similar to [findRenderedDOMComponentWithClass](http://facebook.github.io/react/docs/test-utils.html#findRenderedDOMComponentWithClass), find one component in the tree that has a certain class name. If none or more than one then throws an error.

```javascript
ReactComponent findWithClass(ReactComponent tree, string className)
```
