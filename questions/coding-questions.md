# Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
will print 1020
this is asking the variable to concatinate an integer (10) with a string of text (20).


*Question: What will be the output of the code below?*
```javascript
console.log(0.1 + 0.2 == 0.3);
```
false. 
this is asking if 0.2 is equal to 0.3, due to the order of operations.
if the equation was writtern ((0.1+0.2) == 0.3), we would receive True. 

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```


*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
split i,',m,a,,l,a,s, etc.. creates an array from this string, and includes spaces in the commas
reverse returns an exact copy of this format with commas as an array
join takes this array and makes it a string again.
so we receive back "goh angasal a m'i" with spaces

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```
why is this always 'bar' according to github.com/utatti/???

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
inner alert = "hello world"
outer alert is undefinded - it cannot access the variable bar, since that is a local not global variable

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
the length of the array "foo" is 2. the push operations simply added in 2 elements, which happen to be integers.

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
``


*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
this will print one, three, two.
this is because console.log(one) fires, then console.log(three), then the setTimeout fires AFTER those two. 



*Question: What is the difference between these four promises?*
```javascript
doSomething().then(function () {
  return doSomethingElse();
});

doSomething().then(function () {
  doSomethingElse();
});

doSomething().then(doSomethingElse());

doSomething().then(doSomethingElse);
```
