// --- Directions
// Check to see if two provided strings are anagrams of eachother.
// One string is an anagram of another if it uses the same characters
// in the same quantity. Only consider characters, not spaces
// or punctuation.  Consider capital letters to be the same as lower case
// --- Examples
//   anagrams('rail safety', 'fairy tales') --> True
//   anagrams('RAIL! SAFETY!', 'fairy tales') --> True
//   anagrams('Hi there', 'Bye there') --> False

// // MY SOLUTION (SOLUTION 2)
// function anagrams(stringA, stringB) {
//   let removedA = stringA.replace(/[^\w]/g, "")
//   let removedB = stringB.replace(/[^\w]/g, "")
//
//   let strA = removedA.toLowerCase().split('').sort().join('')
//   let strB = removedB.toLowerCase().split('').sort().join('')
//
//   return strA === strB ? true : false
// }

// SOLUTION 1
function anagrams(stringA, stringB){
  let arrayA = stringA.replace(/[^\w]/g, "").toLowerCase().split('')
  let arrayB = stringB.replace(/[^\w]/g, "").toLowerCase().split('')

  let objA = {}
  let objB = {}

  for(let char of arrayA){
    objA[char] ? objA[char]++ : objA[char] = 1
  }

  for(let char of arrayB){
    objB[char] ? objB[char]++ : objB[char] = 1
  }

  if(Object.keys(objA).length !== Object.keys(objB).length) return false

  for(chunk in objA){
    if(objA[chunk] !== objB[chunk]) return false
    }
  return true
}
module.exports = anagrams;
