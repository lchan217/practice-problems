// --- Directions
// Implement classes Node and Linked Lists
// See 'directions' document

class Node {
  constructor(data, next = null){
    this.data = data
    this.next = next
  }
}

class LinkedList {
  constructor(){
    this.head = null
  }

  insertFirst(data){
    //this.head -> existing node to pass in
    //then reassign this.head to the newly created node
    const newNode = new Node(data, this.head) //puts new node in front of existing head
    this.head = newNode // officially assigns it to head
  }

  size(){
    let count = 0
    let node = this.head

    while(node){
      count++
      node = node.next
    }
    return count
  }

  getFirst(){
    return this.head
  }

  getLast(){
    if (!this.head){
      return null
    }

    let node = this.head
    while(node){
      if(node.next === null){
        return node
      }
      node = node.next
    }
  }

  clear(){
    //if linked list doesn't have a head, it isn't a list
    this.head = null
  }

  removeFirst(){
    if(!this.head){
      return
    }
    this.head = this.head.next
  }

  removeLast(){
    //list is empty?
    if (!this.head){
      return
    }

    //list is 1?
    if (!this.head.next){
      this.head = null
      return
    }

    // else?
    let previous = this.head
    let current = this.head.next
    while(current.next){
      previous = current
      current = current.next
    }
    previous.next = null
  }

  insertLast(data){
    const last = this.getLast()

    if (last){
      last.next = new Node(data)
    } else {
      this.head = new Node(data, this.head)
    }
  }

  getAt(n){
    let counter = 0;
    let current = this.head

    while(current){
      if (counter === n){
        return current
      }
      counter ++
      current = current.next
    }
    return null
  }

  removeAt(n){
    //length = 0
    if (!this.head){
      return
    }

    if(n === 0){
      // you had this.head === null, but it's unnecessary...just need to reassign head
      this.head = this.head.next
      return
    }

    const previous = this.getAt(n-1)
    if(!previous || !previous.next){
      return // out of bounds? getAt() returns null & previous wouldn't exist
    }
    previous.next = previous.next.next //(.next.next - skip 1 node)
  }

  insertAt(data, n){
    //length = 0
    if(!this.head){
      this.head = new Node(data)
      return
    }

    //insert at first index
    if(n === 0){
      this.head = new Node(data,this.head)
      return
    }

    const previous = this.getAt(n-1) || this.getLast() //getLast covers for out of bounds case
    const node = new Node(data, previous.next)
    previous.next = node
  }

  forEach(fn){
    let current = this.head
    let counter = 0

    while (current){
      fn(current, counter)
      current = current.next
      counter++
    }
  }

    *[Symbol.iterator]() {
    let node = this.head;
    while (node) {
      yield node;
      node = node.next;
    }
  }
}

//getFirst/Last methods - can hard code getAt() with 0...way to abstract it and create less code

module.exports = { Node, LinkedList };
