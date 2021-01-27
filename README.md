# The Weather App

Please following the instructions in the book chapter to build this app.

## Get started
You can build on this repo after install the required node packages with "npm install".
You can also create a new project as follows:
```
expo init weather
```
and choose the "blank" template. Note: on Windows you may need to use the `--template` flag on the command-line to choose the template.
```
expo init weather --template blank
```

```
cd weather
expo start
```
This starts the app. Then you can choose to use "Tunnel" or "LAN" as the connection and run the starter app on your phone.
You should see "Open cup App.js to start working on your app!"

If you don't see the "Metro Bundler" webpage popping, try typing http://localhost:19002 (whatever "Expo DevTools URL provided in the command-line ) in your browser to manually bring up the interface.

## Notes

In order to use a Component, it needs to be imported using the "import" statements.

A custom component can be a [function component](https://www.reactnative.express/react/components/function_components) or a [class component](https://www.reactnative.express/react/components/class_components).

A function component receives `props` via the input parameter. A class component can access its `props` using `this.props`. The keyword `this` refers to the class component instance.

You can lookup React Native built-in Core Components in [React Native API specifications](https://reactnative.dev/docs/components-and-apis).

We can pass functions to components as `props` to handle events that happen to the components.

Because `props` are "owned" by its parent, they are immutable. For a component store/remember mutable data, which changes over time, we must define and initialize `this.state` in the class component constructor and should _always_ use `setState` to modify the state. A stateless component is called a _representational_ component because its job is to "present" data given by the parent component.

The `constructor` method is called before the component is _first_ mounted/instantiated, so it should be used to initialize state. The `render` method is called whenever the view needs to be updated as an reaction to state change, e.g. the view presents data derived from the state.

React Navtive provides "lifecycle methods" we can override to "hook" into lifecycles events, in which components are instantiated, changed, or destroyed. `componentDidMount()` is called _after_ the component is mounted, so it is common to trigger network requests to fetch data that the component would need. For a visual reference, check out [this lifecycle diagram](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/).

To log messages to JavaScript console, you can use `console.log()`, `console.warn()`, or `console.error()` according the severity of the messages.
