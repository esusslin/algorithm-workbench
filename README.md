# algorithm-workbench

JS algo workbench repo w notes

## Big-O Notation

#### Constant Time - O(1)

A single operation, regardless of input size

```javascript
function printFirstItem(items) {
  console.log(items[0]);
}
```

#### Linear Time = O(n)

1 to 1 ratio of input : work

worst case runtime assumes O(n)

```javascript
function printAllItems(items) {
  items.forEach(item => {
    console.log(item);
  });
}

// worst case

function contains(haystack, needle) {
  // Does the haystack contain the needle?
  for (let i = 0; i < haystack.length; i++) {
    if (haystack[i] === needle) {
      return true;
    }
  }

  return false;
}
```

#### Quadratic Time = O(n^2)

n to (n \* n( ratio of input : work

(even if there are slight variances to the 'double' factor)

```javascript
function printAllNumbersThenAllPairSums(numbers) {
  console.log("these are the numbers:");
  numbers.forEach(number => {
    console.log(number);
  });

  console.log("and these are their sums:");
  numbers.forEach(firstNumber => {
    numbers.forEach(secondNumber => {
      console.log(firstNumber + secondNumber);
    });
  });
}
```
