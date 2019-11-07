// --- Directions
// Print out the n-th entry in the fibonacci series.
// The fibonacci series is an ordering of numbers where
// each number is the sum of the preceeding two.
// For example, the sequence
//  [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
// forms the first ten entries of the fibonacci series.
// Example:
//   fib(4) === 3

// //SOLUTION 1 (iterative)
// function fib(n) {
//   let array = [0,1]
//   for(let i = 2; i <= n ; i++){
//     const a = array[array.length-1]
//     const b = array[array.length-2]
//     array.push(a+b)
//   }
//   return array[n]
// }

// //solution 2 (recursive)
// function fib(n){
//   if(n < 2){
//     return n
//   }
//   return fib(n-1) + fib(n-2) // see tree diagram ~4 min
//   // breaking everything down until you reach fib(1) and fib(0)
//   // count up all the fib(1)'s (which equals 1) and that's the answer
//   // exponential runtime... how to improve process? memoization
// }

//solution 3 (memoization) NEED TO REWATCH
function slowFib(n){
  if (n < 2){
    return n
  }

  return fib(n - 1) + fib(n - 2)

}

function memoize(fn){
  const cache = {}
  return function (...args){
    // ...args - not sure how many args there will be, so accept all

    //have we called this function with an argument already calculated? if so return cache[args]
    if (cache[args]){
      return cache[args]
    }

    //we need to calculate with new arg and store it so we don't have to calculate again
    const result = fn.apply(this, args)
    cache[args] = result
    return result
  }
}

const fib = memoize(slowFib)

// Memoization: store arguments of each function call along with the result.
// If function is called again with same args, return precomputed result
// rather than running the function again.

module.exports = fib;
