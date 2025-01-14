# State, Events and Forms: Interactive Components

```bash
npx create-react-app@5 steps
cd steps
code .
```

- Delete everything except `App.js` and `index.js`.
- Delete extra files like reportWebVitals.
- Get vanilla.html and index.css from starter files.

Rules of hooks:

- You can only call them at the top level of the component
- Can't call them inside if statements

## Don't Set State Manually!

Always use the setter function to update state.
In the Stepper example, we changed the destructured array to a let and then changed 'step' manually. And the app doesn't do anything anymore because React is not aware that the state is changing.

Just now: In React, a view is updated by re-rendering the component everytime the state changes.

## React Developer Tools

Download Chrome Extension.

## Updating State Based on the Current State

Instead of doing something like: `if (step > 1) setStep(step - 1)`

We should pass a callback function with the current value of the state: `if (step > 1) setStep((s) => s - 1)`
