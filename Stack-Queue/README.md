# Stacks and Queues

## Stacks

#### A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

````js
class Stack {
 constructor() {
   this.stack = [];
 }
 push(item) {
   this.stack.push(item);
 }
 pop() {
   this.stack.pop();
 }
}
```

# Queues

## Queues follow these concepts:

#### FILO First In Last Out

#### This means that the first item added in the stack will be the last item popped out of the stack.

#### LIFO Last In First Out

#### This means that the last item added to the stack will be the first item popped out of the stack

```js
function Queue() {
  this.queue = {};
  this.tail = 0;
  this.head = 0;
}

// Add an element to the end of the queue.
Queue.prototype.enqueue = function (element) {
  this.queue[this.tail++] = element;
};

// Delete the first element of the queue.
Queue.prototype.dequeue = function () {
  if (this.tail === this.head) return undefined;

  var element = this.queue[this.head];
  delete element;
  return element;
};
````
