# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)



SUSAN DUMPING HER CODE:
import './App.css';

const App = () => {
const name = null;
const isNameShowing = true;

  return (
    <div className="App">
        <h1>Hello, {isNameShowing ? name : 'World'}!</h1>
        {name ? (
          <>
            test!
          </>):(
            <>
            <h1>test</h1>
            <p>if you want to render two different elements next to e/o, need to wrap them in react fragments</p>
            </>
          )}
    </div>
  );
}

export default App;


/////////////
const Person = (props) => {
  return(
  <>
    <h1>First Name : {props.name}</h1>
    <h2>Last Name : {props.last}</h2>
    <h2>Age : {props.age}</h2>
  </>
  )
}
const App = () => {
  return (
    <div className="App">
      <Person name={'John'} last={'Doe'} age={30}/>
      <Person name={'Sara'} last={'Murphy'} age={12}/> ///this is important because imagine there are a bunchhh of users and they have a bunchh of attributes
    </div>
  );
}
//////////
import {useState} from 'react';
import './App.css';
const App = () => {
  const[counter, setCounter]=useState(0); //the useState hook to make dynamic modifications
  return (
    <div className="App">
      <button onClick={() => setCounter((prevCount)=>prevCount-1)}>-</button>
      <h1>{counter}</h1>
      <button onClick={() => setCounter((prevCount)=>prevCount+1)}>+</button>
    </div>
  );
}
///////////
const App = () => {
  
  const[counter, setCounter]=useState(30); 
  useEffect(()=>{ //useEffect is pulled as a function that accepts a function as a parameter
    alert(" changed the counter to "+ counter);
  },[counter]) //when the dependency array is empty, the code inside useEffect function is only going to happen initially
  return (
    <div className="App">
      <button onClick={() => setCounter((prevCount)=>prevCount-1)}>-</button>
      <h1>{counter}</h1>
      <button onClick={() => setCounter((prevCount)=>prevCount+1)}>+</button>

    </div>
  );
}
/////////


