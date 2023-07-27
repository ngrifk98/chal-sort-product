# Nick's Code Challenge - Array Sorting by Product and Index

Hey there! I'm Nick, and I completed this code challenge to sort an array of integer numbers based on the product of the value and the index. The task was to sort the array in ascending order, where the index starts at 1 (NOT at 0).

## Challenge Description

The challenge was to create a JavaScript function that takes an array of integers as input and returns the sorted array based on the product of each element's value and its index.

Here's an example to illustrate how the sorting works:

### Input:

Array: [23, 2, 3, 4, 5]

Product of value and index:

- 23 => 23 * 1 = 23
- 2 => 2 * 2 = 4
- 3 => 3 * 3 = 9
- 4 => 4 * 4 = 16
- 5 => 5 * 5 = 25

### Output:

Sorted Array: [2, 3, 4, 23, 5]

## Solution

To solve this challenge, I followed these steps:

1. Created a new array of objects, where each object contains the original value, the product of value and index, and the original index (to maintain the order).
2. Sorted the array of objects based on the product of value and index.
3. Extracted the sorted values from the array of objects to get the final sorted array.

## Code Example

```js
function sortArrayByProductAndIndex(arr) {
  const arrayWithProducts = arr.map((value, index) => ({
    value,
    product: value * (index + 1),
    originalIndex: index,
  }));

  arrayWithProducts.sort((a, b) => a.product - b.product);

  const sortedArray = arrayWithProducts.map((obj) => obj.value);

  return sortedArray;
}

// Example usage
const inputArray = [23, 2, 3, 4, 5];
const sortedArray = sortArrayByProductAndIndex(inputArray);
console.log(sortedArray); // Output: [2, 3, 4, 23, 5]
```

Feel free to use the `sortArrayByProductAndIndex` function in your own projects whenever you need to sort an array based on the product of value and index.

I hope you find this code useful! If you have any questions or suggestions, feel free to reach out. Happy coding! 🚀