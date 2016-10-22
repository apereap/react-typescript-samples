# 01 Hello React

In this sample we are going to setup the basic to work with React.

We will start from sample 00 Boilerplate.

Summary steps:
- Install dependencies
- Create a react render.

Let's ensure we have installed the previous sample dependencies

```
npm install
```

It's a good idea as well to install globally webpack and TypeScript Definition:

```
npm install webpack -g
```

```
npm install tsd -g
```

## Required dependencies
- *00 Boilerplate* dependencies
- bootstrap
- jquery
- react
- react-dom

Let's install all them:

```
npm install bootstrap jquery react react-dom --save
```

# React render

let's going to move the body from src/index.html to the
file called _index.tsx_.

## Definition
#### src/index.tsx

```javascript
import * as React from 'react';
import * as ReactDOM from 'react-dom';

ReactDOM.render(
    <div className="container-fluid">
        <div className="row about-page top-buffer">
          <h1 className="jumbotron">01 Hello React</h1>

          <div className="col-xs-12">
            <h1>
              <small>
                This sample takes as starting point sample "00 Boiler plate".
              </small>
            </h1>
            <div className="col-xs-12">
                <h3>
                    <small>
                        We add on top of that sample a simple react render.
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
                <h4><b>Index:</b></h4>
                <ul className="top-buffer">
                  <li>
                    <h4>
                      index.tsx: <small>react + reactDom imports and simple dom render.</small>
                    </h4>
                  </li>
                </ul>
              </li>
            </ul>
          </div>
        </div>
    </div>
  , document.getElementById('root'));
```

- **imports**: describes which *dependencies* this module has.
- **ReactDOM.render**: instantiates the root component, starts the framework,
 and injects the markup into a raw DOM element, provided as the second argument.

## Using React Render
### src/index.html

Now we are going to change the body and insert <div id="root">.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>Hello webpack !</h1>
    <div id="root">
    </div>
  </body>
</html>
```

We use *id="root"*, that we defined previously in *ReactDom.render* second argument.

Let's run the sample

```bash
npm start
```
