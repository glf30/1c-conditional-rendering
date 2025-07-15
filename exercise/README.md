# Conditional Rendering Exercise

## Exercise Overview

We are going to build a weather-themed React application that demonstrates conditional rendering. This exercise will guide you through creating a toy app with various methods of conditional rendering to show different weather conditions like cloud cover, rain, and temperature. We'll also use Bootstrap to make our app look visually appealing.

## Set Up a New Vite Project

1. Open VS Code and then open the terminal with in the `exercise` directory by right-clicking on this `readme.md` file and selecting **Open in Integrated Terminal**.
2a. In Terminal, type `npm vite weather-conditions-app` followed by return. Here we are naming our project `weather-conditions-app`. 
2b. It may prompt you if you want to install Vite. You can hit return, confirming first that it says `vite` and not a misspelling.
2c. It will prompt you to "Select a Framework". Choose React.
2d. It will prompt you to "Select a Variant". Choose JavaScript.
3. Then open the folder in VS Code by choosing File -> Open Folder and selecting the folder `weather-conditions-app`.

## Install Bootstrap

4. Next, let's import Bootstrap, a front-end framework that provides CSS code to make our project beautiful. Launch a new terminal using Terminal -> New Terminal or using Ctrl+`. In your terminal, type `npm i bootstrap@5.2.3`. This will install the package into our project.

## Import Bootstrap

5. Then in VS Code, open the **/src/main.jsx** file and import the Bootstrap CSS by typing the following line `import 'bootstrap/dist/css/bootstrap.css';`, placing it just after the import for ReactDOM and just before our import for **index.css**. This way we can override the Bootstrap styles with our own inside **index.css** if we wish to.

## Start Node Test Server

6. In Terminal, type `npm run dev` to start a node server. This should give you a message that the Local is **localhost:5173**. This is a clickable link to open it in your default browser, but you can go to the URL manually if you prefer.

## Creating the App Component

Setup your app to look like this

```jsx
  return (
	<div className="App container mt-5">
	  <div className="row">
		{/* YOUR CODE HERE */}
	  </div>
	</div>
  );
```

## Applying CSS Classes

13. Erase the text "Weather Conditions" from inside the `div`. Add the attribute `className="container mt-5"` inside the `<div>`.
14. Inside the `<div>`, create another `<div>` and give it the Bootstrap class name of `row`.
15. Add comments inside the `<div>` with the class name `row` to make a note of what will eventually go there.

## Creating Nested Components

Let's create components for the three weather conditions: CloudCover, Rain, HotTemperature, and ColdTemperature.

16. In a new `components` folder, create a file called `CloudCover.jsx`.
17. Create another file in the same location and name it `Rain.jsx`.
18. Create another file in the same location and name it `HotTemperature.jsx`.
19. Create another file in the same location and name it `ColdTemperature.jsx`.

#### CloudCover.js

```jsx
import React from 'react';

function CloudCover() {
  return (
    <div className="card text-center">
      <div className="card-body">
        <h5 className="card-title">Cloud Cover</h5>
        <p className="card-text">It's cloudy today.</p>
      </div>
    </div>
  );
}

export default CloudCover;
```

#### Rain.js

``` jsx
import React from 'react';

function Rain() {
  return (
    <div className="card text-center">
      <div className="card-body">
        <h5 className="card-title">Rain</h5>
        <p className="card-text">It's raining today.</p>
      </div>
    </div>
  );
}

export default Rain;
```

#### HotTemperature.js

```jsx
import React from 'react';

function HotTemperature() {
  return (
    <div className="card text-center">
      <div className="card-body">
        <h5 className="card-title">Hot Temperature</h5>
        <p className="card-text">It's hot today with a temperature above 60°F.</p>
      </div>
    </div>
  );
}

export default HotTemperature;
```

#### ColdTemperature.js

```jsx
import React from 'react';

function ColdTemperature() {
  return (
    <div className="card text-center">
      <div className="card-body">
        <h5 className="card-title">Cold Temperature</h5>
        <p className="card-text">It's cold today with a temperature below 60°F.</p>
      </div>
    </div>
  );
}

export default ColdTemperature;
```

## Using let-declared Variable with if for `CloudCover`

Use an `if` statement to conditionally render the `CloudCover` component.

## Using Short-Circuit && Evaluation for Rain

Next, we'll use logical AND (&&) to conditionally render the `Rain` component.

## Using Ternary Operator for Temperature

We'll use the ternary operator to conditionally render either the `HotTemperature` or `ColdTemperature` component.  We'll say it's hot if it's greater than 60 degrees or else it's Cold (for all intents and purposes).

## Conclusion

In this exercise, we learned how to conditionally render components in React using different methods like `if` statements, the short-circuit `&&` operator, the ternary operator, and inline expressions. We also used Bootstrap to style our app and make it visually appealing. You can now use these techniques to create more complex applications with conditional rendering in React.
