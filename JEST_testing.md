# Testing React Components

## Shallow
Real unit test (isolation, no children render)
This need to be your first options. Always think on making unit test, if you
need other method that can be replaced with shallow, then go for it.


### Simple testing with shallow

Calls:

- constructor
- render

### Testing Shallow + setProps

Calls:

- componentWillReceiveProps
- shouldComponentUpdate
- componentWillUpdate
- render

### Shallow + unmount

Calls:

- componentWillUnmount

### Mount

The only way to test componentDidMount and componentDidUpdate.
Full rendering including child components.
Requires a DOM (jsdom, domino).
More constly in execution time.
If react is included before JSDOM, it can require some tricks:

`require('fbjs/lib/ExecutionEnvironment').canUseDOM = true;`

### Simple mount

Calls:

- constructor
- render
- componentDidMount

### Mount + setProps

Calls:

- componentWillReceiveProps
- shouldComponentUpdate
- componentWillUpdate
- render
- componentDidUpdate

### Mount + unmount

Calls:

- componentWillUnmount

### Render
It only calls render but renders all children.
There is no need to use render in Unit Testing, at least some specific cases.
For example, some instances of HOCs.


## A simple rule for a good practices
So my rule of thumbs is:

- Always begin with shallow
- If componentDidMount or componentDidUpdate should be tested, use mount
- If you want to test component lifecycle and children behavior, use mount
- If you want to test children rendering with less overhead than mount and you
  are not interested in lifecycle methods, use render

# Doubts

There seems to be a very tiny use case for render. I like it because it seems
snappier than requiring jsdom but as @ljharb said, we cannot really test React
internals with this.

I wonder if it would be possible to emulate lifecycle methods with the render
method just like shallow ?

I would really appreciate if you could give me the use cases you have for
render internally or what use cases you have seen in the wild.

I'm also curious to know why shallow does not call componentDidUpdate.

