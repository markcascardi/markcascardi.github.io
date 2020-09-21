---
layout: post
title:      "Arrow function what’s your function"
date:       2020-09-21 04:40:09 +0000
permalink:  arrow_function_what_s_your_function
---


Two guys walk into a bar and one guy says to the other guy, he says, “What’s the difference between a regular function and an arrow function”?  The other guy (it’s me, I’m the other guy) mumbles something about ‘this’ and ‘binding’, and realizes he can’t quite put it into words.  So they have a couple of socially distanced drinks, go home, and read about arrow functions in ES6.

![](https://i.imgur.com/C87xx6T_d.webp?maxwidth=728&fidelity=grand)

So I was on to something about the arrow function and what it means for ‘this’.  Maybe I can elaborate…Arrow functions do not have their own `this`, rather arrow functions determine what `this` is based on the scope of where the arrow function is defined.  Unlike regular functions, they do not default to window scope.  This makes code more readable and intuitive.  For example, we can now use an arrow function for DOM-level functions without having to use the `bind` method to establish scope like we would with a regular function.

In React this makes arrow functions useful when passed as an event handler.  

This code will work:

```
  handleOnClick = () => {
    console.log(this.props.value);
  };

  render() {
    return (
      <button onClick={this.handleOnClick}>Hello!</button>
    );
  }

```

The reason the this works is because the scope of `this` is where the function is defined.

And this will not:

```
  handleOnClick = function() {
    console.log(this.props.value);
  };

  render() {
    return (
      <button onClick={this.handleOnClick}>Hello!</button>
    );
  }
```

The reason the second code snippet will not work is because `this` is defined when the function is invoked.

Another syntax feature that makes the arrow function easier to read is a that single line arrow functions can be written without curly braces AND without an explicit return statement.  If the arrow function has some other logic in it that before returning, you need to use an explicit return statement.  While this isn't the main reason you use an arrow function, it does help to clean up your code.

For short functions this is a nice improvement, and here's a quick example.

Regular function:
```
const add = function(x, y) { 
  return x + y
}

```

Arrow function:
```
let add = (x, y) => x + y;

```

To summarize, the main reason we use arrow functions in React is that arrow functions automatically binds this to the surrounding code's context.  There are a couple of other reasons, and all of them result in simpler and more readable code.  So the "next" time someone asks me about functions as I'm walking into a bar, I'll have an actual answer (but still no punchline).
