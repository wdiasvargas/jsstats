_For an in-depth look at the API, go [here](API.md)._

## How to use js.stats ##
The js.stats API is meant to be extraordinarily simple. Using the function _stats()_, you specify the requested command followed by a string of numbers. You can also use an array of numbers. The function will return the answer.

For example:
```
<script type="text/javascript" src="http://jsstats.googlecode.com/files/js.stats-latest.js"></script>
<script type="text/javascript">
var data = "1.6, 2.5, 3.1, 4.2, 5.8";

var answer = stats("median", data);

alert("The answer is " + answer);  // The answer is 3.44
</script>
```

The alert box will display the median, in this case 3.44.


## Available functions ##
Currently you can request the following descriptive statistics:
| **Request**          | **Function**                |
|:---------------------|:----------------------------|
| Count                | `stats("count", data)`      |
| Mean                 | `stats("mean", data)`       |
| Median               | `stats("mean", data)`       |
| Minimum              | `stats("min", data)`        |
| Maximum              | `stats("max", data)`        |
| Standard Deviation   | `stats("st_dev", data)`     |
| Standard Error       | `stats("st_dev", data)`     |
| Sum                  | `stats("sum", data)`        |
| Variance             | `stats("variance", data)`   |




## Determining decimal places ##
By default, _stats()_ will always return the answer to two decimal points. By setting a variable called `decimal_places` you can override the default value to anything you wish. Negative values are permitted. The code for this is:
```
var data = "1.6, 2.5, 3.1, 4.2, 5.8";
var decimal_place = 0;

var answer = stats("mean", data_array);

alert("The answer is " + answer);  // The answer is 3
```

The answer is 3, rounded from 3.44.

_Note: this feature is not available (and not necessary) for count(), max(), min(), and sum()_.