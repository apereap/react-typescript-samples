# 02 Components

Let's get started working with components.

In this demo will create a common header and about page react components.

We will start from sample **01 Hello React**.

Summary steps:
- Refactor App component.
- Create Header component
- Create AboutPage component

## Required dependencies
- *01 Hello React* dependencies

```
npm install
```

# Header component

This is a simple header component.

## Definition:
### src/components/common/header.tsx

We have to create a src subfolder called components and inside another folder
called common.

Let's create the file _header.tsx_.

```
import * as React from 'react';

interface Props extends React.Props<Header> {
}

// Nice tsx guide: https://github.com/Microsoft/TypeScript/wiki/JSX
export default class Header extends React.Component<Props, {}> {
   public render() {
       return (
        <div className="row">
          <h2> Application Header</h2>
        </div>
       );
  }
}
```

# App component

We are going to create a Header component inside App component, so it will
appear in all views from our application.

## Definition:
#### src/components/app.tsx

Let's create a new file _app.tsx_ inside src/components and we are going to
include the new component Header.

```
import * as React from 'react';
import Header from './common/header';

interface Props extends React.Props<App> {
}

// Nice tsx guide: https://github.com/Microsoft/TypeScript/wiki/JSX
export default class App extends React.Component<Props, {}> {
   public render() {
       return (
        <div className="container-fluid">
          <Header/>
        </div>
       );
  }
}
```

# About component

This is a simple about page component.

## Definition:
### src/components/about/about.tsx

We have to create a src/components subfolder called about.

Let's create inside the file _aboutPage.tsx_.

```
import * as React from 'react';

interface Props extends React.Props<About> {
}

// Nice tsx guide: https://github.com/Microsoft/TypeScript/wiki/JSX
export default class About extends React.Component<Props, {}> {
   public render() {
       return (
           <div className="row about-page top-buffer">
             <h1 className="jumbotron">02 Components</h1>

             <div className="col-xs-12">
               <h1>
                 <small>
                   This sample takes as starting point sample "01 Hello react".
                 </small>
               </h1>
               <div className="col-xs-12">
                   <h3>
                       <small>
                           We are adding react components: a main component that consumes a header and aboutPage component.
                       </small>
                   </h3>
               </div>
             </div>

             <div className="col-xs-12 top-buffer">
               <h3>Highlights</h3>
               <hr/>
               <h3>
                 <small>
                   The most interesting parts worth to take a look
                 </small>
               </h3>
             </div>

             <div className="col-xs-12 top-buffer">
               <ul>
                 <li className="top-buffer">
                   <h4><b>Components:</b></h4>
                   <ul className="top-buffer">
                     <li>
                       <h4>
                         app.tsx: <small>main component, instantiates header and common component.</small>
                       </h4>
                     </li>
                     <li>
                       <h4>
                         header.tsx: <small>simulate a header component (in next samples this will include a nav bar).</small>
                       </h4>
                     </li>
                     <li>
                       <h4>
                         aboutPage.tsx: <small>page like component.</small>
                       </h4>
                     </li>
                   </ul>
                 </li>
               </ul>
             </div>
           </div>
       );
  }
}
```

# App component

We are going to create an about component inside App component.

## Configuration:
#### src/components/app.tsx

Let's include the AboutPage component in _app.tsx_. Don't forget the import.

```
import * as React from 'react';
import Header from './common/header';
import AboutPage from './about/aboutPage';
...
<div className="container-fluid">
  <Header/>
  <AboutPage/>
  </div>
...
```

# Using App component

We are going to use App component from _index.tsx_.

## Configuration:
#### src/index.tsx

Let's import App and use as the first argument of ReactDOM.render.

```
import * as React from 'react';
import * as ReactDOM from 'react-dom';
import App from './components/app';

ReactDOM.render(
  <App/>
  , document.getElementById('root'));
```

Let's run the app:

```
npm start
```
