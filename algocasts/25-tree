
// --- Directions
// 1) Create a node class.  The constructor
// should accept an argument that gets assigned
// to the data property and initialize an
// empty array for storing children. The node
// class should have methods 'add' and 'remove'.
// 2) Create a tree class. The tree constructor
// should initialize a 'root' property to null.
// 3) Implement 'traverseBF' and 'traverseDF'
// on the tree class.  Each method should accept a
// function that gets called with each element in the tree

class Node {
  constructor(data){
    this.data = data
    this.children = []
  }

  add(data){
    const newNode = new Node(data)
    this.children.push(newNode)
  }

  remove(data){
    this.children = this.children.filter(node => {
      return node.data !== data
    })
  }
}

class Tree {
  constructor(){
    this.root = null //like the head for linked lists
  }

  traverseBF(fn){
    const array = [this.root]
    while (array.length){
      const node = array.shift() //remove first element
      for (let child of node.children){
        array.push(child) //add to end
      } // or array.push(...node.children)

      fn(node)
    }
  }

  traverseDF(fn){
    const array = [this.root]
    while (array.length){
      const node = array.shift() //remove first element
      array.unshift(...node.children) //add to start
      fn(node)
    }
  }
}

module.exports = { Tree, Node };
