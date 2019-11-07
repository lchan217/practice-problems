// --- Directions
// Write a function that accepts a positive number N.
// The function should console log a step shape
// with N levels using the # character.  Make sure the
// step has spaces on the right hand side!
// --- Examples
//   steps(2)
//       '# '
//       '##'
//   steps(3)
//       '#  '
//       '## '
//       '###'
//   steps(4)
//       '#   '
//       '##  '
//       '### '
//       '####'

// // SOLUTION 1- use this unless specifically asked for recursion
// function steps(n) {
//   //diagram in lecture helps
//   // when column is less or equal to row, you get a pound
//   for (let row = 0; row < n; row++){
//     let stair = ''
//     for (let column = 0; column < n; column++) {
//       if (column <= row) {
//         stair += '#'
//       } else {
//         stair += ' '
//       }
//     }
//       console.log(stair)
//   }
// }

// SOLUTION 2 - recursion
function steps (n, row = 0, stair = ''){
  //base case #1
  if (n === row) {
    return
  }

  //we are at the end of the row
  if (n === stair.length) {
    console.log(stair)
    steps(n, row + 1)
    return
  }

  // if stair length is less than or equal to row number, add #
  // else add space
  if (stair.length <= row){
    stair += "#"
  } else {
    stair += " "
  }
  steps(n, row, stair)
}

module.exports = steps;
