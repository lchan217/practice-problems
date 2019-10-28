// --- Directions
// Write a function that returns the number of vowels
// used in a string.  Vowels are the characters 'a', 'e'
// 'i', 'o', and 'u'.
// --- Examples
//   vowels('Hi There!') --> 3
//   vowels('Why do you ask?') --> 4
//   vowels('Why?') --> 0

// //SOLUTION 1
// function vowels(str) {
//   let count = 0
//   const vowelLetters = "aeiou"
//   for (let char of str.toLowerCase()){
//     if (vowelLetters.includes(char)){
//       count++
//     }
//   }
//   return count
// }

//SOLUTION 2
function vowels(str) {
  // g - makes sure we don't stop at 1st match
  // i - case insensitive
  const matches = str.match(/[aeiouAEIOU]/gi) // returns array of matches; if nothing - returns null
  return matches ?  matches.length : 0
}

module.exports = vowels;
