---
title: JavaScript Arrays Are Just Objects 
author: Ryan McDermott
layout: post
---

JavaScript arrays are super handy for making dynamic lists with any type of
content. If you come from another language like Java or C++, arrays are
contiguous blocks of memory where each item has to be of the same type. When
they are of the same type, the computer can know the `sizeof` that type and know
how to find the next item in the array by incrementing a pointer in memory based
on `sizeof` type. Since JavaScript doesn't have types, how exactly do arrays
work?

The answer: JavaScript arrays are just objects with integer keys! Don't believe
it, let's take a look at some code examples.

```javascript
const realArr = ["foo", "bar"];
realArr[3] = "baz";
console.log(realArr); // [ 'foo', 'bar', <1 empty item>, 'baz' ]
```

When `'baz'` is added to the array above, as the 4th item, there's implictly an
empty key for the 3rd item since nothing was added.

Arrays also act like objects in that you can add any property to it. Let's take
a look at how:

```javascript
const realArr = ["foo", "bar"];
realArr.example = "hello";
console.log(realArr); // [ 'foo', 'bar', example: 'hello' ]
```

Arrays and objects can also be seen as equals when looking at what happens when
you try to get the keys for a real array and a "fake" array.

```javascript
const realArr = ["foo", "bar"];
const fakeArr = { 0: "foo", 1: "bar" };
console.log(Object.keys(realArr)); // [ '0', '1' ]
console.log(Object.keys(fakeArr)); // [ '0', '1' ]
```

Because arrays are just objects, you can actually add onto an object all the
methods and properties you would find on an array like `push`, `pop`, and
`length`. In doing so, you can create a fake array! Let's see how that is done:

```javascript
class FakeArray {
  constructor(...items) {
    let arr = {};
    arr.length = 0;
    for (let i = 0; i < items.length; i++) {
      arr[i] = items[i];
      arr.length++;
    }

    arr.push = function(item) {
      this[this.length] = item;
      this.length++;
    };

    arr.pop = function() {
      let val = this[this.length - 1];
      delete this[this.length - 1];
      this.length--;
      return val;
    };

    return arr;
  }
}

let arr = new FakeArray("foo", "bar");

console.log(arr); /*
                    { 0: 'foo',
                      1: 'bar',
                      length: 2,
                      push: [Function],
                      pop: [Function] }
                  */

console.log(arr[1]); // bar
console.log(arr.length); // 2

arr.push("baz");
console.log(arr); /*
                   { 0: 'foo',
                     1: 'bar',
                     2: 'baz',
                     length: 3,
                     push: [Function],
                     pop: [Function] }
                  */

console.log(arr.pop()); // baz
console.log(arr.length); // 2

console.log(arr.pop()); // bar
console.log(arr.length); // 1

console.log(arr.pop()); // foo
console.log(arr.length); // 0
```
