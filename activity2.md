
# Built-in Methods To Iterate Through An Array: Arrays Are Also [Magic Marry Poppins Bags:](https://www.youtube.com/watch?v=AivZSC9J3Rs&feature=share) And The Built-In `filter()` Method

<sup> Activity 2/3  </sup>

## Learn
JavaScript has a number of important built-in methods. In the previous activity we learned about the  `.forEach()`  method which iterates through an array and does something with each item in the array. JavaScript has several other useful "work your way through the array and do things" built-functions, including:

- every (stops looping the first time the iterator returns false or something falsey)
- some (stops looping the first time the iterator returns true or something truthy)
- filter (creates a new array including elements where the filter function returns true and omitting the ones where it returns false)
- map (creates a new array from the values returned by the iterator function)
- reduce (builds up a value by repeated calling the iterator, passing in previous values; see the spec for the details; useful for summing the contents of an array and many other things)
- reduceRight (like reduce, but works in descending rather than ascending order)

 A complete list of Array methods can be found [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/).

One of the most common tasks when working with an array is to create a new array that contains a subset of elements of the original array. JavaScript has another cool built-in method that helps us do this, it is the `filter()` method.

The `filter()` method creates a new array by filtering out all the elements that do not pass the test implemented by the callback() function. Internally, the filter() method iterates over each element of an array and pass each element to the callback() function. If the callback() function returns true, the element is included in the resulting array. It is used like this



```javascript
var words = ["spray", "limit", "elite", "exuberant", "destruction", "present"];

var longWords = words.filter(function(word){
  return word.length > 6;
})

console.log(longWords)

//["exuberant", "destruction", "present"]
```

In this case:

1. The `filter()` method creates a new array with all elements that pass the test implemented by the provided function. 
2. The test is the line of code `word.length > 6`, which returns any element of the array that has more than 6 letters.
3. The `log` of longWords shows a new array made up of all the elements from the original `words` array that have more then 6 letters. ` ["exuberant", "destruction", "present"]`

## Instructions
Arrays can hold more then just strings, in fact arrays can hold almost anything you can think of! In that way, JavaScript arrays are like a magic bag! But things can get messy inside a bag that can hold anything, so it's important to have a way to sort through the items in the bag to be able to find what you are looking for.

In the code editor there is an array called `magicBag`

``` javascript
var magicBag = [

{thing:"toothpaste", importance: 1},
{thing: "towel", importance: 2},
{thing: "magic wand", importance: },
{thing: "bowling ball", importance: },
{thing: "hat stand", importance: 3},
{thing: "lamp", importance: 3},
{thing: "plant", importance: },
{thing: "tape measure", importance:1 },
{thing: "hat stand", importance: 1},
{thing: 28, importance: 3}

  ]

```



#### 1. Use the filter() method to make an array of items in the magic bag that have more then 6 letters.

### Hint
Did you create a new variable named `longWords` to hold the new array of items that pass the `filter()` method test? Did you `return` any item's `thing` that is more then 6 characters long?


```  javascript
var longWords = magicBag.filter(function(item){
  return item.thing.length > 6;
})
```

***

  #### 2. Use the `filter()` method to create an array of only the most important items, those with an importance value of 1.


```  javascript
var importantItems = magicBag.filter(function(thing){
  return thing.importance ===1;
})

  console.log(importantItems)

  //returns an array with 4 items

  var importantItems = [
  {thing:"toothpaste", importance: 1},
{thing: "magic wand", importance:1 },
{thing: "tape measure", importance:1 },
{thing: "hat stand", importance: 1},
]
```

## Let's Review
Magic bags and dream concerts are great and all, but what about some real life applications of JavaScript's built-in methods for iterating through arrays?! In the next activity we will learn how to use JavaScript built-in methods to create content on an actual website! Press 'Next' to continue.
<!-- 
4. ??? Something really crazy and exciting?!?! Or just more about othe rbuilt in methods and move on and then do something really weird and exciting in ex. 3?
Use the `filter` method to......
create an array named magicBag and add at least 4 items to it. You will of course, want to make sure one of those things is a towel, because as The Hitchhiker's Guide To The Galaxy says, 

> "A towel, it says, is about the most massively useful thing an interstellar hitchhiker can have."

### Hint/ Example Code
``` javascript
var magicBag = ["toothpaste", "towel", 1, 1, 2,3,5,8,  ]

```


## What You Got In That Bag?!

use the forEach method you learned in the dream concert activity to show a list of everything that is in your magic bag
``` javascript

magicBag.forEach(function(item){
    console.log(item)
})

```


//b we can even hold arrays inside arrays! So to make my packing neater I can create avariable to hold an array of my fibonnaci sequence and then put that variable in my array
var fib = [1, 1, 2,3,5,8,]

var magicBag = ["toothpaste", "towel", fib  ]

//notice now that you get a much neater list of items with the entire set of fib numbers as one contained thing
magicBag.forEach(function(item){
    console.log(item)
})

Another important thing Thie Hitchhiker's Guide To The Galaxy says is: 

> "to know where one's towel is" means to be in control of one's own life. "

So let's find your towel!

console.log(magicBag.indexOf('towel'))

You should probably have your towel as the first thing in your bag, just in case!

{{how to move towel to 0 index position}}

//No matter where you are giong on your trip, there are a few items that you will need no matter what. For example, what if it rains where you are? Or what if you run into an evil wizard? 

//add to your magic bag, an item to protect you from the rain, and a magic wand-or otherwise magically embued item.


magicBag.push('rain coat', 'magic wand')
//notice that you can push multiple items at once by seperating them with a comment
console.log(magicBag)

//Before we dump more awesome things into our bag, let's see how many items we already have in our bag. 

//Knowing the length of an array is useful as feedback, as in this example where we are using magicBag.length to understand how many items we have, and it is also useful programmatically as it can be used to form other functions (and inform other methods?). For more on the length() method of arrays see https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length
console.log(magicBag.length)
//preparing for...


//checking to see if we packed something
//wait did I pack my magic wand?
console.log(magicBag.includes('magic wand'))
console.log(magicBag.join())
//phantom tollbooth style missions with the magic bag

// 8 – Get a random item from an array

var items = [12, 548 , 'a' , 2 , 5478 , 'foo' , 8852, , 'Doe' , 2145 , 119];

var  randomItem = items[Math.floor(Math.random() * items.length)];


// * find something in particular
// * find a random item
// *pull the first item
//* pull a particular item

//* travel light mode! use .slice( ) to just take some objects with you

//* sort() to get through customs


//* a land where everything is backwards

//* Create a secret code to only show the contents of your bag to people who have the password. Otherwise return random characters from array + 'nice try muggle!'


/*Methods to develop story for*/

// .concat() -->