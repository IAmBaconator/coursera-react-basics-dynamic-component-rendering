# coursera-react-basics-dynamic-component-rendering
A demo application to demonstrate rendering a component based on the current state of the data when a user logs in or logs out of the app.
* **State management** in React allows components to track and update dynamic data, such as whether a user is logged in or not.<br/>
* **Props** passing enables parent components to send data or functions to child components, like passing login and logout functions to buttons.<br />
* **Conditional rendering** controls what appears on the screen based on the current state, such as showing a login button when logged out or a home page with a logout button when logged in.
## Goal
To practice using React’s `useState` hook to manage the logged-in state and conditionally render components based on that state.
# Lab Notes
Command to create _(this)_ React app, `npx create-react-app toggle_app` and start the browser preview of the app, `npm start`.<br />
**Note:** The  `create-react-app` command is deprecated.
## LoginButton Explaination
* Simple functional component.
* Receives a login function through a prop and binds it to an onClick event.
* Clicking the button will trigger a change in the application state.
## LogoutButton Explaintion
* Simple functional component.
* Receives a logout function through a prop and binds it to an onClick event.
* Clicking the button will trigger a change in the application state.
## HomePage Explaination
* Functional component that rendors an `h1` message statically.
## App Explaination
### State Management:  
* The `useState` hook (`const [loggedIn, setLoggedIn] = useState(false)`) is used to define and manage the `loggedIn` state.
* `loggedIn` is a boolean that determines the current login status.
### Functions:
* The login function (`const login = () => setLoggedIn(true);`) sets `loggedIn` to true, and the logout function (`const logout = () => setLoggedIn(false);`) sets it to false.
### Conditional Rendering:
* When loggedIn is false, the LoginButton is displayed by calling the LoginButton component(`<LoginButton login={login} />`).
* When loggedIn is true, the HomePage and LogoutButton are displayed by calling the HomePage (`<HomePage />`) and LogoutButton (`<LogoutButton logout={logout} />`) components.
### Props Passing:
* The login and logout functions are passed as props to LoginButton and LogoutButton, respectively.  