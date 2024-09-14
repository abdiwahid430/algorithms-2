function insertionSort(arr) {
  // Iterate over each element in the array starting from the second element
  for (let i = 1; i < arr.length; i++) {
    // Store the current element to be inserted
    let current = arr[i];
    // Initialize the position for comparison
    let j = i - 1;

    // Move elements of the sorted portion that are greater than the current element
    // to one position ahead of their current position
    while (j >= 0 && arr[j] > current) {
      arr[j + 1] = arr[j];
      j--;
    }

    // Insert the current element into its correct position
    arr[j + 1] = current;
  }

  return arr;
}

// Example usage
const array = [5, 2, 9, 1, 5, 6];
console.log(insertionSort(array)); // Output: [1, 2, 5, 5, 6, 9]
