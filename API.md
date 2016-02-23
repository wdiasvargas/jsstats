## Introduction ##
The function _stats()_ acts as a clearing house for all other functions in the library. It handles data scrubing, handles errors, and uses a simple _switch_ statement to determine which request to use. _stats()_ will **always** return a numeric value unless there is an error, in which case it will return a string of text.


## Parameters ##
_stats()_ accepts three parameters: `request`, `data`, and `data2`. `request` determines which statistical command to run. `data` and `data2` are strings of numbers that make up the datasets. Only `data` is required and the user does not need to include a parameter for `data2` if s/he does not wish to.

For example, if the user wants the median value of a series of numbers, the following code will create an alert box with the answer:
```
var data = "1, 4, 6, 7, 7, 12";

var answer = stats("median", data);

alert("The answer is " + answer);  // The answer is 6.50
```


## Error handling ##
When the wrong data is passed to _stats()_ the function will return "ERROR: " followed by a plain English error message.

For example, if a user tries to pass the array [apple, banana, orange] s/he would get the following response:
```
var data = "apple, banana, orange";

var answer = stats("median", data);

alert(answer);  // "ERROR: apple is not a number"
```