---
title: 'React: Tic-Tac-Toe'
date: 2023-12-25 23:01:20
tags: [react]
---
This artical is a quick note of the [react tic tac toe tutorial](https://react.dev/learn/tutorial-tic-tac-toe). You can use this aritcal as a reminder of the key points of this tutorial.

# App.js
```javascript
export default function Square() {
  return <button className="square">X</button>;
}
```
* export: make this function accessible outside of this file.
* default: tell other files that this is the main function of this file
* \<button\>: a JSX element. JSX element = JS code + HTML tags. It describes what you like to display
* classname="square": button property, tells CSS the style of the button
* X: text of the button

# styles.cs
This is to determine how each part looks like.

# index.js
This is the bridge between the component in ```App.js``` and the web browser

# Building the board
* Fragments: <></>
    This is used to wrap multiple adjacent JSX elements
* `<div></div>`: group elements into rows

# Passing data through props
"Prop" is like argument in other programming language.
Below is an example of passing props:
```JavaScript
function Square({ value }) {
  return <button className="square">{value}</button>;
}

export default function Board() {
  return (
    <>
      <div className="board-row">
        <Square value="1" />
        <Square value="2" />
        <Square value="3" />
      </div>
      <div className="board-row">
        <Square value="4" />
        <Square value="5" />
        <Square value="6" />
      </div>
      <div className="board-row">
        <Square value="7" />
        <Square value="8" />
        <Square value="9" />
      </div>
    </>
  );
}

```

# Making an interactive component

