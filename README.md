# React Native Calculator
This is a simple calculator project built using React Native.

## How to run
To run this project, simply clone this repository and execute the following commands:

## Install dependencies
```
npx install react-native
```
or
```
npm install -g expo-cli
```

# Run the application
With the terminal open and in the application directory, type:

```
npx react-native run-android
```
or
```
npx react-native run-ios
```

# Components
## Button
The `Button` component is responsible for rendering a button on the calculator screen. It receives the following parameters:

- label: The text that will be displayed on the button;
- double (optional): A boolean value that indicates whether the button should be twice the standard size;
- triple (optional): A boolean value that indicates whether the button should be three times the standard size;
- operation (optional): A boolean value that indicates whether the button is an operation (such as +, -, *, and /).

## Display
The `Display` component is responsible for rendering the calculator display. It receives a single parameter:
- value: The value that will be displayed on the display.

## App
The `App` component is the main component of the application. It renders the Display and Button components, and implements the calculator logic.

# Initial state
The initial state of the calculator is defined by the `initialState` constant and has the following structure:

```
const initialState = {
  displayValue: '0',
  clearDisplay: false,
  operation: null,
  values: [0, 0],
  current: 0
}
```

# Methods
The `App` component defines three methods:
- addDigit(n): Adds a digit to the value displayed on the display. If the digit is a dot and there is already a dot in the value, nothing is done. If the current value is 0, the display is cleared before adding the digit.
- clearMemory(): Clears the calculator memory, restoring the initial state.
- setOperation(operation): Defines the operation to be executed and updates the calculator state according to the selected operation.

# Rendering
The `App` component renders the `Display` and `Button` components according to the current state of the calculator. The buttons are organized in a grid with 4 columns and several rows, using the style defined in the `style` object.
