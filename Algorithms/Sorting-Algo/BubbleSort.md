# Bubble Sort

Bubble sort sorts an array, by swapping elements that are in the wrong order. It starts from the first element in the array until the last element in the array, and keeps on doing so until there is one entire pass without swapping! This creates a “bubble” effect, hence the name.

## Time Complexity

Best -> O(n) = Linear

Worst -> O(n2) = quadratic

### CODE 1

```function BubbleSort(array) {
  for (let i = 0; i < array.length; i++) {
    for (let j = 1; j < array.length; j++) {
      if (array[j] < array[j - 1]) {
        swap(array, j, j - 1);
      }
    }
  }
  return array;
}

function swap(array, index1, index2) {
  let temp = array[index1];
  array[index1] = array[index2];
  array[index2] = temp;
}

console.log(BubbleSort([1, 4, 2, 5, 8, 9, 4])); // [1,2,4,4,5,8,9]
```

### Code 2 optimal

```
function bubbleSort(array) {
  let swap;
  do {
    swap = false;
    for (let i = 0; i < array.length; i++) {
      if (array[i] && array[i + 1] && array[i] > array[i + 1]) {
        const temp = array[i];
        array[i] = array[i + 1];
        array[i + 1] = temp;
        swap = true;
      }
    }
  } while (swap);
  return array;
}

console.log(bubbleSort([1, 4, 3, 2])); // [1,2,3,4]
```
