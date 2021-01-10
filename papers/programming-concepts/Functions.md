# Functions, Return Data and Passing Data

Functions are a method of processing data or executing code in the same way multiple times, but with different parameters.

A function is declared, usually with parentheses following it, and curly brackets containing the code of the function.

```javascript
  function addAndLog(num1, num2) {
    let result = num1 + num2;
    console.log(result);
    return;
  }
```

The above example is written in javascript, and it adds two numbers and logs the result to the console. The advantage of a function is that we can use this function as many times as we want, and simply pass different parameters each time.

```javascript
  addAndLog(5, 21);
  addAndLog(17, 3);
  addAndLog(51, 6);
```

Anything you can code outside a function can be coded inside a function, which makes functions very powerful. You can think of a function like a car manual. Usually the manual will apply to multiple variations of your model, therefore it will continain multiple rules for each variety. Now if the manual were a function, the parameters inside the parentheses (the data passed to it) would be the car's model, and the function would return the resulting instructions.

```javascript
  function changeOil(model) {
    let instructions = {
      oilType,
      amount,
      filterNumber
    }
    if(model == "abc") {
      instructions.oilType = "Type1";
      instructions.amount = "5L";
      instructions.filterNumber = "101";
      
    } else if(model == "def") {
      instructions.oilType = "Type2";
      instructions.amount = "5L";
      instructions.filterNumber = "100";
    }
    
    return(instructions);
  }
```

The above code takes the vehicle model as a parameter and returns the correct information to do an oil change.

Note: the `return` method is how we access the result of a function from outside the function. For example, if we did:

```javascript
    let instructions = changeOil("def");
```

`instructions` would be equal to the data that the `changeOil` function returned via the `return` method.

Many languages require functions to be defined by their return type.

```cpp
    int main() {
      
      return 0;
    }
```

The above code is C++ (or C given the example). The `main` function is declared as an `int` or an integer, and it returns `0` which is an integer. 

```cpp
  string greet(string name) {
    string greeting = "Hello, " + name;
    return greeting;
  }
```

The above function, `greet` is declared with the return type `string` because it returns a `greeting` which is a string.
