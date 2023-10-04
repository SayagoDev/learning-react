# Learning React

## Components as building blocks

- React applications are entirely made out of components
- **Building blocks** of user interfaces in React
- Piece of UI that has its own **data**, **logic**, and **appearance** (_how it
  works and looks_)
- We build complex UI by **building multiple components** and **combining** them
- Components can be **reused**, **nested** inside each other, and **pass data**
  between them

## What is JSX?

- **Declarative** syntax to **describe** what components **looks like** and
  **how they work**
- Components must **return** a block of JSX
- Extension of JavaScript that allows us to **embed JavaScript, CSS and React
  components into HTML**
- Each JSX element is **converted** to a `React.createElement` function call
- We could use React **without JSX**

### JSX is declarative

#### 🚫 Imperative —How to do things—

- Manual DOOM element selections and DOM traversing
- Step-by-step DOM mutations until we reach the desired UI

#### ✅ Declarative —What we want—

- Describe what UI should looks like using JSX, **based on current data**
- React is an **abstraction** away from DOOM: **we never touch the DOOM**
- Instead, we think of the UI as a **reflection of the current data**

## Props

- Props are used to pass data from **parent components** to **child components
  (**down\*\* the component tree)
- Essential tool to **configure** and **customize** components (like function
  parameters)
- With props, parent components **control** how child components look and work
- **Anything** can be passed as props: single values, arrays, objects,
  functions, even other components

### Props are **READ-ONLY!**

- Props is data coming from the **outside**, and can **only** be updated by the
  **parent component**.
- State is internal data that can be updated by the **component's** logic
- 👆 Props are read-only, they are **immutable!** This is one of React's stric
  rules
- 👆 If you need to mutate props, you actually **need state**

#### Why?

- 👉 Mutating props would affect parent, creating **side effects** (not pure)
- 👉 Components have to be **pure functions** in terms of props and state
- 👉 This allows React to optimize apps, avoid bugs, make apps predictable

### One-way data flow

In React applications, data can only be passed from parent to child components,
which happends by using props. Data can flow from parents to children, but never
the opposite way. Therefore, we have a one way data flow, only from top to
bottom of the component tree.

One-way data flow...

- 👍 ...makes applications more predictable and easier to understand
- 👍 ...makes applications easier to debug, as we have more control over the data
- 👍 ...is more performant
