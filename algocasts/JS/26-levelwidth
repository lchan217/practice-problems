// --- Directions
// Given the root node of a tree, return
// an array where each element is the width
// of the tree at each level.
// --- Example
// Given:
//     0
//   / |  \
// 1   2   3
// |       |
// 4       5
// Answer: [1, 3, 2]

//see 'width' in problem? think breadth-first

function levelWidth(root) {
  const counters = [0] //holds width
  const array = [root, 'string'] //holds tree, 'string' can be anything, whenever we see it, it's one level

  while(array.length > 1){ // 'string' will always be there
    const node = array.shift()

    if(node === 'string'){
      counters.push(0) //initialize counter for next level
      array.push('string')// push 'string' to end to signify new level
    } else {
      array.push(...node.children)
      counters[counters.length-1]++ //increment by length by 1
    }
  }
  return counters
}

module.exports = levelWidth;
