# Vocab Review

Sometimes we know things without knowing it has a name. These are some terms you will want to be familiar with as you start interviewing.

## Process 
- SDLC - Systems/Software Development Life-Cycle. How a project goes from idea to implementation. 
    References: [Tutorials Point](https://www.tutorialspoint.com/sdlc/sdlc_overview.htm), [Wikipedia](https://en.wikipedia.org/wiki/Systems_development_life_cycle)

- TDD - Test Driven Development. The development practice of writing tests first to drive the process of writing application code. 
    References: [FreeCodeCamp](https://medium.freecodecamp.org/test-driven-development-what-it-is-and-what-it-is-not-41fa6bca02a2), [TDD Example Walkthrough](https://technologyconversations.com/2013/12/20/test-driven-development-tdd-example-walkthrough/)

- Single Page Application (SPA) - Web applications that load a single HTML page and then dynamically update that page using Ajax,as the user interacts with the application. 
    References: [How Single Page Apps Work](https://medium.com/@pshrmn/demystifying-single-page-applications-3068d0555d46), [Wikipedia](https://en.wikipedia.org/wiki/Single-page_application)

- Retrospective - A meeting where the project team is able to reflect on the past project or sprint. The team identifies specific things to stop doing, continue doing, & start doing, in order to create a plan for improvements to be enacted for the next project or sprint.
    References: [Scrum Retrospective](https://www.scrum.org/resources/what-is-a-sprint-retrospective), [Running a Retrospective w/ Examples](https://www.atlassian.com/team-playbook/plays/retrospective)

- Agile - Development process built on an incremental, iterative approach. Instead of in-depth planning at the beginning of the project, Agile methodologies are open to changing requirements over time, encouraging constant feedback from the end users.
    Resources: [What is Agile?](https://www.smartsheet.com/agile-vs-scrum-vs-waterfall-vs-kanban#what-is-agile)


- Scrum - A subset of Agile that uses an iterative model with fixed-length iterations, called sprints, which allow the team to ship software on a regular cadence. At the end of each sprint, stakeholders and team members meet to plan next steps. 
    Resources: [What is Scrum?](https://www.smartsheet.com/agile-vs-scrum-vs-waterfall-vs-kanban#what-is-scrum)

- Waterfall - A linear development process where a project progresses from stage to stage sequentially. Once one of the stages is complete, the team moves onto the next step. If anything from an earlier stage changes the entire process must begin again.
    Resources: [What is Waterfall?](https://www.smartsheet.com/agile-vs-scrum-vs-waterfall-vs-kanban#what-is-waterfall)

- Kanban - Is a visual project managment framework used to implement Agile that utilizes a task board with swim lanes to show the status of tasks (i.e. waiting to start, in progress, & done). Traditionally this is a physical board with paper notes, but it could also be digital. 
    Resources: [What is Kanban?](https://www.smartsheet.com/agile-vs-scrum-vs-waterfall-vs-kanban#what-is-kanban)

- Backlog
- Backlog Grooming
- User Story
- Ticket
- Estimation
- DevOps

## React 

- Function Component - The simplest type of React component. A function that accepts props and returns a React element (JSX).
    Example:
    ```JavaScript
    const Header = ({ title }) => (
      <div className="instructions">
        <div>
          <h1 className="lead">{ title }</h1>
        </div>
      </div>
    );
    ```
    Reference: [React Docs: Components & Props](https://reactjs.org/docs/components-and-props.html)

- props - set of properties that are passed into a component.
    Reference: [React Docs: State FAQ](https://reactjs.org/docs/faq-state.html)

- state - set of properties that are managed *within* a component. 
    Reference: [React Docs: State FAQ](https://reactjs.org/docs/faq-state.html)

- render - The only required method in a React class component. The method should return the React components (JSX) to render on the DOM.
    Reference: [React Docs: Render](https://reactjs.org/docs/react-component.html#render)

- component lifecycle - the component lifecycle is a set of methods that are called on components by the React framework at specific times. These methods provide developers a set of hooks to run component code at particular times.
    Reference: [React Docs: Component Lifecycle](https://reactjs.org/docs/react-component.html#the-component-lifecycle)

- HOC - Higher Order Component. Component that takes in a  component and returns back another which extends its behavior. 
  Example:
  ```JavaScript
  import {withRouter} from 'react-router-dom';
  class MyButton extends Component {
    handleClick = () => {
      // History is added to the component by 'withRouter'
      this.props.history.push('/newPage')
    } 
    render() {
      return (
        <button onClick={this.handleClick} />
      )
    }
  }
  export default withRouter(AnimalButton);
  ```

## JavaScript/Programming

- function - A function is a callable, repeatable stack of code. It may take in one or more inputs, and may return output.

- argument/parameter - input to a function. Technically in the definition of the function it is called a parameter. The actual value passed into the function is an argument.
    Example: 
    ```JavaScript
    myFunction(param1, param2) { 
      // do something
    }
    let arg1 = "foo";
    let arg2 = "bar";
    myFunction(arg1, arg2);
    ```
    References: [Stack Overflow](https://stackoverflow.com/questions/156767/whats-the-difference-between-an-argument-and-a-parameter), [Wikipedia](https://en.wikipedia.org/wiki/Parameter_(computer_programming))

- return value - the output of a function, or what the function returns back to the calling code.

- function declaration - Way to define a function. It will "hoist" the definition so that you can use it in the file before it is defined.
    Example:
    ```JavaScript
    function doubleItBetter(x) {
      return x * 2;
    }
    ```

- function expressions - A way to define a function, basically you have a variable and give it a (anonymous) function as its value.
    Example: 
    ```JavaScript
    // function expression
    let doubleIt = function(x) {
      return x * 2;
    }
    ```

- anonymous function - A function that doesn't get a name. They are often used to handle events. 
    Example: 
    ```JavaScript
    $('#myButton').on('click', function() {
      console.log('Clicked the button');
    });
    ```

- module - a reusable piece of JavaScript code which exports specific objects, making them available for other modules to require in their programs.
    Example:
    **movies.js**
    ```JavaScript
    const favMovies = [
        'Harry Potter',
        'Case of Benjamin Button',
        'Ace Ventura',
        'Groundhog Day',
        'Willow'
    ];

    function logMovies() {
        for(let movie of favMovies) {
            console.log(movie);
        }
    }

    module.exports = {
        displayMovies: logMovies
    }
    ```
    **main.js**
    ```JavaScript
    console.log('Show the movies:')
    let moviesModule = require('./movies');
    moviesModule.displayMovies();   
    ```
    References: [Free Code Camp - JS Modules a Beginner's Guide](https://medium.freecodecamp.org/javascript-modules-a-beginner-s-guide-783f7d7a5fcc)

- object - An object is a collection of properties, where a property is a name (or key) and value pair. 
    Example: 
    ```
    let myCar = {
        make: 'Ford',
        model: 'Mustang',
        year: 1969
    }
    ```
    References: [MDN Developer Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects), [Wikipedia](https://en.wikipedia.org/wiki/Object_(computer_science))

- class - in OOP (object-oriented programming), a class is a template for creating objects, providing initial values for state (member variables) and implementations of behavior (member functions or methods).
    Example:
    ```JavaScript
    class Car {
        constructor(make, model, year){
            this.make = make;
            this.model = model;
            this.year = year;
        }
        start(){
            console.log(`Starting the ${this.year}  ${this.make} ${this.model}`);
        }
        stop(){
            console.log(`Stopping the ${this.year}  ${this.make} ${this.model}`);
        }
    }
    ```
    Reference: [MDN Developer Guide - Classes in JS](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes), [Wikipedia - OOP Classes](https://en.wikipedia.org/wiki/Class_(computer_programming))

- prototype - A template object from which other objects may inherit properties.    Reference: [MDN Developer Guide](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes) 

- generator function - A function which can be exited and later re-entered with its context (variable bindings) saved across re-entrances. We have used generator functions in React Sagas.
    Example: 
    ```JavaScript
    function* myGenerator() {
        yield 1;
        yield 2;
        yield 3;
    }
    //create an instance
    const inst = myGenerator();
    // call generator with .next()
    console.log(inst.next()); // 1
    console.log(inst.next()); // 2
    console.log(inst.next()); // 3
    ```
    References: [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*), [Wikipedia](https://en.wikipedia.org/wiki/Generator_(computer_programming))

- currying - a function that returns a function. More specifically, it is breaking down a function that takes multiple arguments into a series of functions that take a part of the arguments. We have used this to pass parameters to event handlers.
    Example: 
    ```JavaScript
    // Need function that takes an event for the event handler,
    // but we also want to know the name of the property to change
    handleChangeFor = (propertyName) => {
      // returns a function that takes an event
      return (
        (event) => {
          this.setState({
            newCreature: {
              ...this.state.newCreature,
              // the propertyName is plugged in here
              // before the function is returned
              [propertyName]: event.target.value,
            }
          })
        }
      );
    }
    ```
    References: [Stack Overflow](https://stackoverflow.com/questions/36314/what-is-currying), [Wikipedia](https://en.wikipedia.org/wiki/Currying)

- conditional
- data type
- algorithm
- iterator
- collection
- event 
- event handler

- destructuring - JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.
    Example: 
    ```JavaScript
    ```
    Refrences: [MDN: Object Destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Object_destructuring), [MDN: Array Destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Array_destructuring)

- API - Application Programming Interface - a set of functions and procedures allowing that access the features or data of an operating system, application, or other service.
    Example: [Giphy API](https://developers.giphy.com/docs/)
    Reference: [Wikipedia](https://en.wikipedia.org/wiki/Application_programming_interface)

- MVC
- MVVM

- JSON - JavaScript Object Notation - syntax used in JS to create object literals. It has two main structures: objects with key/value pairs & arrays
    Reference: [Introducing JSON](https://www.json.org/)

- IDE - Integrated Development Environment - software for programming that generally includes a editor with syntax highlighting and intelligent code-completion for source code & a debugger, and may also include build tools and/or source code management tools.

### Concepts

- What's the difference between host objects and native objects in JavaScript?
- Explain "hoisting". What is the difference between `let` and `var`?
    References: [FreeCodeCamp: Variable Hoisting](https://medium.freecodecamp.org/what-is-variable-hoisting-differentiating-between-var-let-and-const-in-es6-f1a70bb43d), 
    [FreeCodeCamp: Function Hoising & Interview Questions](https://medium.freecodecamp.org/function-hoisting-hoisting-interview-questions-b6f91dbc2be8)

## Web
- CMS - Content Management System - system that manages the creation and publication of digital content. Often this is used specifically to refer to the creation and management of web content.
    Examples: [Top CMS of 2018](https://www.bluleadz.com/blog/the-8-best-marketing-cms-platforms-in-2018)
    References: [Wikipedia: CMS](https://en.wikipedia.org/wiki/Content_management_system), [Wikipedia: Web CMS](https://en.wikipedia.org/wiki/Web_content_management_system)

- cookies
- session
- token
- request 
- response
- ajax

- asynchronous - Processes that are happening concurrently or at the same time. One process does not have to complete before the next one may begin.
    Reference: [Wikipedia](https://en.wikipedia.org/wiki/Asynchrony_(computer_programming))

- HTTP
- HTTPS/TLS/SSL
 
- proxy - a stand in for someone/something - Typically refers to a proxy server, which acts as an intermediary for client requests, forwarding those to other servers. We have seen this in our React development projects where a proxy is used to forward requests from our client process to our server.
    Resources: [Wikipedia](https://en.wikipedia.org/wiki/Proxy_server), [Setting up a React Node Proxy](https://www.twilio.com/blog/react-app-with-node-js-server-proxy)

- REST - Representational State Transfer - an architectural style for building Web services that are lightweight, maintainable, and scalable. A service based on REST is called a RESTful service. While REST is not dependent on any protocol, they typically use HTTP. 
    References: [Wikipedia](https://en.wikipedia.org/wiki/Representational_state_transfer)

- SOAP - SOAP (Simple Object Access Protocol) - a messaging protocol to exchange structured information for web services. It uses XML for the message format and generally HTTP for message exchange.
    References: [Wikipedia](https://en.wikipedia.org/wiki/SOAP)

- XML - eXtensible Markup Language - A markup language, similar in structure to HTML, which aims to be both human readable and machine readable. Tags are used to markup content, but there is not a fixed set of tags. 
    References: [Wikipedia](https://en.wikipedia.org/wiki/XML)

## Databases
- ERD - Entity Relationship Diagram (aka Entity Relationship Model) - An ERD is a data modeling technique that visually shows a system's entities (objects) and the relationships between those entities. It is often used to design a relational database, but may also be used in a larger system design.
    References: [Wikipedia](https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model), [How to create an ERD](https://www.bridging-the-gap.com/erd-entity-relationship-diagram/)

- entity - An entity is an object or thing. When discussing relational databases, an entity represents a table.

- schema - The formal definition of the database structure, tables with their column names, data types and any constraints and/or relationships.
    References: [Wikipedia](https://en.wikipedia.org/wiki/Database_schema)

- relation - This is NOT a relationship between entities in an ERD. When applied to a database it refers to a table and it's rows of data. 
    References: [Stack Overflow](https://stackoverflow.com/questions/4045744/what-is-a-relation-in-database-terminology)

- primary key
- foreign key

- ORM - Object Relational Mapping - Technique of converting data between the logical representation of the data (objects in code) and an atomized form that is stored in a database. Examples: [Sequelize](http://docs.sequelizejs.com/) & [Mongoose](https://mongoosejs.com/)
    References: [Wikipedia](https://en.wikipedia.org/wiki/Object-relational_mapping)


## Other
- Mock 
- Testing
- Data Structures
- unit test
- greenfield
- brownfield
