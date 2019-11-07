// --- Directions
// Write a function that accepts a positive number N.
// The function should console log a pyramid shape
// with N levels using the # character.  Make sure the
// pyramid has spaces on both the left *and* right hand sides
// --- Examples
//   pyramid(1)
//       '#'
//   pyramid(2)
//       ' # '
//       '###'
//   pyramid(3)
//       '  #  '
//       ' ### '
//       '#####'

//SOLUTION 1
function pyramid(n) {
  // take floor of the mid point... add 1 and subtract 1 for where to add #'s
  const midpoint = Math.floor((2*n-1) / 2)

  for (let row = 0; row < n; row++){
    let level = ''

  // the pattern - 2*n-1 = columns (see diagram)

    for (let column = 0; column < 2*n-1; column++){
      if (midpoint - row <= column && midpoint + row >= column) {
        level += '#'
      } else {
        level +=' '
      }
    }
    console.log(level)
  }
}

module.exports = pyramid;
