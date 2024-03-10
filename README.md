# Login App

## Table of Contents

- [Introduction](#introduction)
- [Dev/Prod Configurations with Vite](#devprod-configurations-with-vite)
- [Husky hooks configured](#husky-hooks-configured)
- [Dependencies](#dependencies)

## Introduction

This project, "Login App," is designed for user authentication and registration. It's built with [Create React App](https://github.com/facebook/create-react-app) and leverages the latest web technologies for a seamless user experience, ensuring that your project is both modern and scalable.

## Features

- **User Registration**: Allows new users to securely create an account.
- **User Login**: Facilitates registered users to securely log in.
- **Responsive Design**: Incorporates Bootstrap for a layout that's attractive on any device.

## Husky Integration

Husky is a tool that allows you to set up Git hooks to automatically run scripts before certain events, such as commits or pushes. This can help you ensure that your code complies with certain style rules and passes testing before being committed to the repository.

### Husky hooks configured

In this project, we have configured the following Husky hook:

- `pre-commit`: This hook is executed before each commit. In our case, we have configured this hook to execute the linting and test commands to ensure that the code complies with the defined standards.

### Installation and configuration

To install Husky in your project, run the following command:

```bash
npm install husky --save-dev
```

## Dependencies

- **Axios**: A promise-based HTTP client for making API requests. It is used in this project to handle HTTP requests and fetch data from the server.

  Example:

  ```javascript
  import axios from 'axios';

  axios
    .get('/api/data')
    .then(response => {
      console.log(response.data);
    })
    .catch(error => {
      console.error(error);
    });
  ```

- **React Router DOM**: A library that provides navigation routing for React applications. It is used in this project to define and manage application routes and views in a declarative way.

  Example:

  ```javascript
  import { BrowserRouter as Router, Route, Routes } from 'react-router-dom';

  function App() {
    return (
      <Router>
        <Routes>
          <Route path='/' element={<Home />} />
          <Route path='/about' element={<About />} />
        </Routes>
      </Router>
    );
  }
  ```

  Documentation: [React Router DOM](https://reactrouter.com/web/guides/quick-start)

- **Redux**: A state management library used to centralize and control data in the application. It enables predictable data flow and facilitates communication between components.

  Example:

  ```javascript
  // Define an initial status and actions
  const initialState = {
    counter: 0,
  };

  const increment = () => ({ type: 'INCREMENT' });

  // Create a reducer
  const reducer = (state = initialState, action) => {
    switch (action.type) {
      case 'INCREMENT':
        return { ...state, counter: state.counter + 1 };
      default:
        return state;
    }
  };

  // Create a store and configure Redux in the application
  import { createStore } from 'redux';

  const store = createStore(reducer);
  ```

  Documentation: [Redux](https://redux.js.org/)

- **Jest**: A unit testing framework for JavaScript. It is used in this project to write and run automated tests to ensure the correct functioning of components and functions.

  Example:

  ```javascript
  // Unit test of a function
  function sum(a, b) {
    return a + b;
  }

  test('sum adds two numbers correctly', () => {
    expect(sum(1, 2)).toBe(3);
  });
  ```

  Documentation: [Jest](https://jestjs.io/)

- **React Testing Library**: A test library that provides tools and utilities for testing React components. It is used in this project to write integration tests and check the behavior of components in different situations.

  Example:

  ```javascript
  import { render, screen } from '@testing-library/react';
  import App from './App';

  test('renders the app component', () => {
    render(<App />);
    const linkElement = screen.getByText(/Hello, World!/i);
    expect(linkElement).toBeInTheDocument();
  });
  ```

  Documentation: [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)

- **Bootstrap**: A popular CSS framework that provides predefined styles and ready-to-use components. It is used in this project to style the user interface.

  Example:

  ```html
  <button class="btn btn-primary">Click me</button>
  ```

  Documentación: [Bootstrap](https://getbootstrap.com/)

- **ESLint**: A linting tool that helps to detect and correct style errors and unwanted practices in the code. It is used in this project to maintain clean and consistent code.

  Documentation: [ESLint](https://eslint.org/)

- **Prettier**: A code formatter that helps to maintain consistent code structure and style. It is used in this project to automatically format code according to the configured style rules.

  Documentation: [Prettier](https://prettier.io/)

- **Moment.js**: JavaScript library for date formatting and manipulation.

  Example:

  ```javascript
  import moment from 'moment';

  const currentDate = moment().format('YYYY-MM-DD');
  ```

  Documentation: [moment](https://momentjs.com/docs/)
