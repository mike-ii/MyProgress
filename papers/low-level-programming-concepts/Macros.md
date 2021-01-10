# Macros

As far as C programming goes, macros can be best described as a method to define a sequence of code which can be repeated throughout the code without having to rewrite the code defined.

Macros are not to be confused with functions, as functions are a sequence of code that is stored in one location and returns data based on the input data. Functions may require a lot of overhead to define the function itself, regardless of the content.

What a macro is, is simply a sequence of code that is more or less copy pasted at every location it's used in the code, based on the rules it was defined with and the values passed to the macro. If I were to write a macro that doubles a number, I could use a macro instead of a function to save resource usage.
```c  
  // Function 
  int double_num(int n) {
    return n * 2;
  }
  
  int num = double_num(2); // 4
  
  // Macro
  
  #define double_num(n) ((n) * (2))
  
  int num = double_num(2); // 4
  
  // The preprossessor simply expands the previous line based on the macros rules, rather than use a whole function 
  // for instance, the above line of code would be:
  
  int num = ((2) * (2)); // 4
```
  
  
In the function example above, the function is stored in memory and a variable is declared as the output of double_num with the integer 2 passed to it. If this process was complex and required a lot of code to complete, then a function would be practical, as the functions overhead is a fair compromise. However, if the task is simple, such as a simple equation, a macro is the better option.

### Magic Numbers

Macros can also be used to prevent the occurrence of [Magic Numbers](https://en.m.wikipedia.org/wiki/Magic_number_\(programming\)) and make code more maintainable. For example, if you have say a number you'd always like to use to declare the size of an array, you can do..
```c
  #define ARRAY_SIZE 128
```
Then whenever you create an array, you can do `arr[ARRAY_SIZE]` instead of `arr[128]` in a hundred different locations. By using a macro to reduce magic numbers, you make the code more maintainable while also making it less confusing.

### Conclusion

Macros can simply be defined as a tool to make the programming process easier. They make code more maintainable, make it less confusing, and allow a light weight method for developers to *not* write the same code over and over. In terms of the resulting executable program, macros don't really make much difference, except in the case of using them in place of a function. Macros just make the human's life easier.


[Source](https://www.computerhope.com/jargon/m/macro.htm#:~:text=A%20macro%20\(which%20stands%20for,a%20preset%20sequence%20of%20output.&text=When%20the%20code%20is%20preprocessed,expanded%20each%20time%20it%20occurs)

  
  
