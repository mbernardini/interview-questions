# Interview Questions

An ever expanding list of possible interview questions.

## General Questions
### JavaScript/TypeScript
 * Explain the difference between `const`, `let` and `var`?
 * What are some JavaScript primitive types?
  * _number, boolean_
 * What is a prototype? What is it used for?
 * Describe how scope resolution in JavaScript works?
 * Explain `bind` and why you would us it?
 * What is a `Promise`?
 * How do you handle errors with promise? How is an exception handled?
 * Explain your understanding of `async`/`await`?
 * What do all `async` functions return?
 * What might be a situation where you'd use a promise over `await`?
  * _Parallel execution (Promise.all) or your target environment doesn't support async/await_
 * What is destructuring? When might you use it?
  * _Syntactic sugar around assignment that allows you directly assign a variable
    from an object or an array._
  * _let {a, b} = JSON.parse("..."); let [value1, value2] = Promise.all(...)_
 * What is a decorator? When might you use it?
  * _A way to change the behavior of a function/class without making changes to the function/class itself._
  * _Use cases: logging, security, validation_
 * What is the spread operator? When might you use it?
  * _`...` aka spread operator allows an iterable to be expanded in place_
  * _Useful for array concatenation/copying, extending objects/copying, calling function (replace apply)_

#### JavaScript WebAPI
* JavaScript interacts with HTML on a webpage using what API?
 * _DOM_
* In a web browser how do you retrieve data from a web server using JavaScript?
 * _The older XMLHttpRequest (XHR) api is an event based API for creating async requests._
 * _The newer `fetch` api is a promised based API that simplifies retrieving data_
 * _WebSockets is also a possibility and is well suited for applications requiring two way communication_
*

### Web Architecture
* What frameworks have you used?
* What do like about framework X? What do you not like?
* If you had to choose a front end framework, which would you choose?
* If you had to choose a server framework, which would you choose?
* Are you familiar with OAuth? Can you explain at a high level how it works?
* Why would you choose to use WebSockets over HTTP or Server Side Events?
* Explain the same-origin policy. How do you get around same-origin policy limitations? Explain how CORS works.
*

### Networking
* What are the two most common transport layer protocols built on top of internet protocol?
* Explain the difference between UDP and TCP? What are some benefits and drawbacks of each?
* What transport layer protocol does HTTP use? How about WebSockets? WebRTC?
  * _TCP_
  * _TCP_
  * _SDP_

### Ops
* How have you managed things like passwords in your code?
* What tools have you used for secrets management?
* Have you heard of the 12 factor app?
* Can you explain your understanding of the 12 factors?

### Functional
* Explain `map`. Explain `flatMap`
* Explain `reduce`

### Project/time management
* How have you handled a project that you thought you could get done by a certain date but as the deadline approached, you realized you would be unable to complete it?
* How do you balance writing tests with a strict project deadline?


## Exercises
### Prefix searching

Suppose that you need to search a list of words to find all words that begin
with a search term. Assume you are given the words in array.

E.g. Given an english dictionary, "sup" => ["superior", "superlative", "supine" ...]

#### Q1: Implement an naive solution

``` javascript
const dict = ["one", "two", "three", "four"];

function search(prefix) {
  const results = [];
  results.forEach(word => {
    if(word.startsWith(prefix)) {
      results.push(word);
    }
  });
  return results;
}

// or perhaps
const search = (prefix) => dict.filter(word => word.startsWith(prefix));
```

###### What is the runtime of your solution? (big O)
_Example code is O(NM) where N is the number of characters in prefix and M is the length of the dictionary_

#### Q2: What are some possible optimizations you might make to the above solution?
TODO: finish

### Find the length of a Line String
TODO: implement

### Triangle Counting
Given N nonparallel lines, implement a function that calculate the number of triangles produced by
intersecting lines. Intersections points are infinitely small and therefore no three lines intersect
at the same point.

TODO: solution
