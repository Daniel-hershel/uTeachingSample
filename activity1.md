# Built-in Methods To Iterate Through An Array: Dream Concert And The Built-In `forEach()` Method
<sup> Activity 1/3  </sup>

## Learn
In JavaScript the Array object lets you store multiple values in a single variable. As humans, we might call this a list. In JavaScript we give the list a title by naming a variable and setting it equal to our array. It is used like this:

``` javascript
var dreamConcert = ["Kendrick Lamar", "Indigo Girls", "Imagine Dragons"]
```

In this case:

1.This is a list of the artists who would make up a dream concert, written as a JavaScript Array.
2. We give our array a title by naming it with a variable.
3. We can now access all the data in our array by the name `dreamConcert`.

Arrays are like lists with super powers. One of the most efficient ways to activate the power of arrays is through the JavaScript idea of *iteration.* In the context of JavaScript, iteration means going through a list of things (an array) and running a block of code for each item in the list.  

JavaScript has a built-in method which makes iterating over an array easy. The `.forEach()` method is well named to help us understand the idea of iteration. The `forEach() `method executes the provided function once for each array element. It is used like this:

``` javascript
dreamConcert.forEach(function(item) {
//do something to each item here
});
```

In this case:
1. `.forEach()` will run the iterator function entered as a parameter for each item in the array named `dreamConcert`.
2. The function will act on of each item in the array into the console. The word 'item' used in this case is a name we have chosen to represent the value of each actual item in our array. You could choose any word you wanted to represent each item in the array, as long as you use it consistantly.

## Instructions

#### 1. In the code editor there is an array named  `dreamConcert` with three items. Adjust the items so that it represents *your* dream concert. Using  `forEach()` , `console.log.` each item in your array.

### Hint
Did you use a `console.log` inside a `forEach()` iterator function to `log` each item in the `dreamConcert` array?

``` javascript
 dreamConcert.forEach(function(item) {
console.log(item);
});
```
 
 ***

 #### 2. In the first example we passed one argument, `item`, into the `forEach()` method which gives us the *value* of each item in the array. The `forEach()` method can also take a second argument, which is the `index` of the current element being processed in the array.It is used like this:

```javascript
 dreamConcert.forEach(function(item, index) {
/*do something with item-the value of each item, and index- the location of each item in the array*/
});
```

By adding the index of each item in your array, we can show people the order in which the peformances will take place at your dream concert. Because arrays count from 0, and we want our dream concert lineup to start at 1 (unless you want a 0 performer at your concert-it is *your* dream concert after all), we will have  to `console.log` `index+1` to have the first performance be listed as 1, instead of 0.

#### Use the `forEach()` method with two arguments: `item` and `index` to console.log the order and names of the performers at your dream concert. 


### Hint
Did you use a `console.log` inside a `forEach()` iterator function to `log` each item and index+1 in the `dreamConcert` array?

``` javascript
 dreamConcert.forEach(function(item, index) {
console.log(index + 1 , item);
});
```

***

#### 3.  Built-in methods like `forEach()` are not the only way in JavaScript to iterate through an array. One that most beginning programmers learn and use is the for loop. So, why use a built-in method over a for loop? 

In the code editor there is an array called `builtInIsBetter` , and a block of code calling the `forEach()` method on that array.
 <!-- write out instructions to this -->

``` javascript
var builtInIsBetter = [

 {title: "More readable", 
details: "the choice of built-in method clearly demonstrates the intended purpose of the loop, in the case of .forEach() we want to iterate through an array without creating a new one"},

{title: "Less boilerplate", details: "writing for loops is unnecessarily monotonous and obfuscates the intention of the code"}, 

{title: "Less room for error", details: " using a built-in method ensures the loop will occur as intended, whereas a for loop is prone to typos"},
{title:"Less scope pollution", details: "each for loop (using var) will declare a variable for its loop; this variable enters the function's scope, adding unnecessary values and potentially overwriting existing variable values"}
]


builtInIsBetter.forEach(function(item, index) {
//console.log('reason #', index+ 1,  item.title + ':'+ item.details);
});

```

In this case:
1. We are calling the `forEach()` method on an array of objects which each have a title and details about that title.
2. Inside our iterator function, which is called to act on each object in our array, we `log` the data from each object in our array.
3. The format for the data is specified inside the paranthesis of the `console.log`.

#### Uncomment the `console.log` line of code in the editor to see some of the reasons to use a built-in method like `forEach()` instead of a for-loop.


### HINT

``` javascript
 builtInIsBetter.forEach(function(item, index) {
console.log('reason #', index+ 1,  item.title + ':'+ ' ' + item.details);
});
```

<!-- expected output -->

> 
> reason # 1 More readable: the choice of built-in method clearly demonstrates the intended purpose of the loop, in the case of .forEach() we want to iterate through an array without creating a new one
> reason # 2 Less boilerplate: writing for loops is unnecessarily monotonous and obfuscates the intention of the code
> reason # 3 Less room for error:  using a built-in method ensures the loop will occur as intended, whereas a for loop is prone to typos
> reason # 4 Less scope pollution: each for loop (using var) will declare a variable for its loop; this variable enters the function's scope, adding unnecessary values and potentially overwriting existing variable values
<!-- Something sending them searching for other iterative methods? -->

## Let's Review...

JavaScript has a built-in method for iterating over arrays called `forEach()`. `forEach()` accepts an iterator function (and, optionally, a value to use as *this* when calling that iterator function-not used above). The iterator function is called for each entry in the array, in order.

The built-in `forEach()` method is a great way to iterate through an array, but it is not the only built-in method that JavaScript has for processing and taking action on elements in an array. We will learn about some of the other built-in iterative methods of JavaScript in the next exercise.

Click 'Next' to continue.

<!-- /*ADDITTIONAL ARRAY METHODS*/ -->

<!-- maybe write these up as *bonus* things you could do with the array at the end of ex. 1? Or make it excersize 2?

/*forEach*/
myMusic.forEach(function(number) {
console.log(number);
});

/*push and pop*/

//push
//forgot to add someone important!
myMusic.push("Bob Marley")

myMusic.forEach(function(number) {
console.log(number);
});

//pop
//want a better gender balance? Or maybe after they play pop them out of the array?


/*indexOf*/
//wanting to know when a band goes on
var whenAmIOn = myMusic.indexOf('Indigo Girls')
console.log(whenAmIOn)


if( whenAmIOn = 1){
    console.log('NEXT!')

} -->