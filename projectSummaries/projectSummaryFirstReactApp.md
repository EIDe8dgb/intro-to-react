Summary of simplest type of React app: `Greeting.html`
1. Goal: create Progressive Web Applications (PWA) and Single-Page Applications(SPA) using React, which is a unidirectional (deterministic), declarative, reusable component-based architecture. The alternative would be using a bidirectional, imperative, MVC-based framework such as Angular, Backbone, or Knockout. Because React uses an internal representation of the DOM (virtual DOM), components rerender automatically with changes in data, and only update the changed elements of a component through its diff-ing algorithm, React apps perform much faster than competing technologies
2. Simplest React app can be created directly within HTML document. Create file called `greeting.html` from command line:
```
>> touch greeting.html
```

3. add basic boilerplate HTML, including DOCtype declaration, html tags, head tags, body tags:
```html
<!DOCTYPE html>
<html>
<head>
    <title>First React app</title>
</head>
<body>
</body>
</html>
```
4. insert React library scripts just before closing `<body>` tag by accessing content delivery network:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Simple React app</title>
</head>
<body>

     <script src="https://cdnjs.cloudflare.com/ajax/libs/react/16.1.0/umd/react.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/16.1.0/umd/react-dom.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.34/browser.min.js"></script>
</body>
</html>
```

5. add opening and closing script tags within `<body>` in which we will code the React component. Specify the type as `text/babel` to activate ES6:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Simple React app</title>
</head>
<body>

     <script src="https://cdnjs.cloudflare.com/ajax/libs/react/16.1.0/umd/react.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/16.1.0/umd/react-dom.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.34/browser.min.js"></script>
     <script type='text/babel'>
     </script>
</body>
</html>
```

6. add a container with id of 'app', which will be the location where the React component is rendered on the page:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Simple React app</title>
</head>
<body>
    <div id='app'></div>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/react/16.1.0/umd/react.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/16.1.0/umd/react-dom.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.34/browser.min.js"></script>
     <script type='text/babel'>
     </script>
</body>
</html>
```

7. within `<script>` tags declare a React component called `Greeting` and give it a `render()` method which returns a "Hello world!" string. Remember that all React components require a `render()` method, and must return a single root element. Thus enclose the returned HTML in a `<div>` tag:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Simple React app</title>
</head>
<body>
    <div id='app'></div>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/react/16.1.0/umd/react.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/16.1.0/umd/react-dom.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.34/browser.min.js"></script>
     <script type='text/babel'>
        class Greeting extends React.Component{
            render(){
                return(
                <div>
                    <h1>Hello World!</h1>
                </div>
                );
            }
        }
     </script>
</body>
</html>
```

8. After the `Greeting` React component, invoke the `ReactDOM.render()` method and specify in the statement that the `render()` function will be rendered within the 'app' div:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Simple React app</title>
</head>
<body>
    <div id='app'></div>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/react/16.1.0/umd/react.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/16.1.0/umd/react-dom.development.js"></script>
     <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.34/browser.min.js"></script>
     <script type='text/babel'>
        class Greeting extends React.Component {
         render() {
           return (
             <div>
               <h1>Hello World!</h1>
             </div>
           );
         }
       }
       ReactDOM.render(
         <Greeting />, document.getElementById('app')
       );
     </script>
</body>
</html>
```
