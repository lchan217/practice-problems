// --- Directions
// Given a string, return the character that is most
// commonly used in the string.
// --- Examples
// maxChar("abcccccccd") === "c"
// maxChar("apple 1231111") === "1"

// use this technique for most common character, does string A have same characters as string B (anagram),
// or are there repeated characters?

// turn string into object where keys - characters, values - count

// for (let char of str) {
//   if (!chars[char]) {
//     chars[char] = 1
//   } else {
//     chars[char]++
//   }
// }
// OR =======================
// for (let char of string){
//   chars[char] = chars[char] + 1 || 1
// }

function maxChar(str) {
  const chars = {};
  let max = 0
  let maxChar = ''

  for (let char of str) {
    chars[char] = chars[char] + 1 || 1
  }

  for (let char in chars) {
    if (chars[char] > max) {
      max = chars[char];
      maxChar = char
    }
  }
  return maxChar
}

module.exports = maxChar;
