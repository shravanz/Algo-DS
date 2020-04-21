# Selection Sort

Selection sort is a simple sorting algorithm, that loops over the array and saves the absolute lowest value. The lowest value is then swapped with the first item in the unsorted array.

## Time Complexity

Best -> O(n2) = quadratic

Worst -> O(n2) = quadratic

### CODE 1

```
function SelectionSort(array) {
  for (let i = 0; i < array.length; i++) {
    let min = i;
    for (let j = i + 1; j < array.length; j++) {
      if (array[j] < array[min]) {
        min = j;
      }
    }
    if (i !== min) {
      [array[i], array[min]] = [array[min], array[i]];
    }
  }
  return array;
}

console.log(SelectionSort([1, 3, 2, 4, 6, 5, 9, 8]));
```
