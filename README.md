## 9. Scoping

- Global Scope
- Local Scope or Function Scope
- Block Scope
- Lexical Scope

#### Global Scope
When you start writing JavaScript in a document, you are already in the Global scope. There is only one Global scope throughout a JavaScript document. A variable is in the Global scope if it's defined outside of a function.

```javascript
// the scope is by default global
var name = 'Suryansh';

console.log(name); // logs 'Suryansh'

function logName() {
    console.log(name); // 'name' is accessible here and everywhere else
}

logName(); // logs 'Suryansh'
```

#### Local Scope
Variables defined inside a function are in the local scope. And they have a different scope for every call of that function. This means that variables having the same name can be used in different functions. This is because those variables are bound to their respective functions, each having different scopes, and are not accessible in other functions.

```javascript
// Global Scope
function someFunction() {
    // Local Scope #1
    function someOtherFunction() {
        // Local Scope #2
    }
}

// Global Scope
function anotherFunction() {
    // Local Scope #3
}
// Global Scope
```

**Note**: Local scope is also called function scope because local scope is created by functions in Javascript. Variables in the local scope are only accessible within the function in which they are defined, i.e they are bound to their respective functions each having different scopes.

#### Block Scope
Block statements like if and switch conditions or for and while loops, unlike functions, don't create a new scope. Variables defined inside of a block statement will remain in the scope they were already in.
```javascript
if (true) {
    // this 'if' conditional block doesn't create a scope

    // name is in the global scope because of the 'var' keyword
    var name = 'Suryansh';
    // likes is in the local scope because of the 'let' keyword
    let likes = 'Coding';
    // skills is in the local scope because of the 'const' keyword
    const skills = 'JavaScript and Node';
}

console.log(name); // logs 'Suryansh'
console.log(likes); // Uncaught ReferenceError: likes is not defined
console.log(skills); // Uncaught ReferenceError: skills is not defined
```

#### Lexical Scope
A lexical scope in Javascript means that a variable defined outside a function can be accessible inside another function defined after the variable declaration. But the opposite is not true, the variables defined inside a function will not be accessible outside that function.

## 10. JavaScript Hoisting


## 11. Window object
