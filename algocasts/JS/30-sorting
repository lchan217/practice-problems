// --- Directions
// Implement bubbleSort, selectionSort, and mergeSort

function bubbleSort(arr) {
  for(let i = 0; i < arr.length; i++){
    for(let j=0; j < (arr.length- i - 1); j++){ //shrinks the array by 1 each time
      if(arr[j] > arr[j+1]){ // if current element > next, then swap
        const lesser = arr[j+1]

        //swap
        arr[j+1] = arr[j]
        arr[j] = lesser
      }
    }
  }
  return arr
}

function selectionSort(arr) {
  for(let i=0; i < arr.length; i++){
    let indexOfMin = i
    for(let j=i+1; j < arr.length; j++){
      if (arr[indexOfMin] > arr[j]){
        indexOfMin = j
      }
    }
    if(indexOfMin !== i){
      let lesser = arr[indexOfMin]

      //swap
      arr[indexOfMin] = arr[i]
      arr[i] = lesser
    }
  }
  return arr
}

function mergeSort(arr) {
  if (arr.length === 1){
    return arr
  }

  const center = Math.floor(arr.length/2)
  const left = arr.slice(0, center) // if arr=['a', 'b', 'c', 'd'] == a & b
  const right = arr.slice(center) // c & d

  return merge(mergeSort(left), mergeSort(right))
}

function merge(left, right) {
  const results = []

  while(left.length && right.length){
    if(left[0] < right[0]){
      results.push(left.shift()) //takes first element out and adds to results
    } else {
      results.push(right.shift())
    }
  }

  //are both arrays empty? combine results with remaining of left and right arrays
  //right could go first too... doesn't matter because 1 is empty and 1 has some left
  return [...results, ...left, ...right]
}

module.exports = { bubbleSort, selectionSort, mergeSort, merge };
