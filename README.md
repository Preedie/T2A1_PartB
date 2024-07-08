# Workbook Part B

# Two Sorting Algorithms

# Gnome Sort

Gnome sort is a simple algorithm that was inspired by the way Gnomes sort flower pots. It's similar to insertion sort however it uses a different approach for the element comparison and swapping process.

## How Gnome Sort Works

1. Gnome sort starts at the beginning of an array (so basically starts at 0)

2. Then gnome sort will compare the current element with the prior one.

- If the current element is higher than the prior (greater) than the previous then the gnome selector will move on to the next element in the array.

- If the current element is lower or smaller than the previous element the gnome selector will swap them and move one step back in the array.

3. The Gnome selector will then continue this process until it reaches the end of the array.

## Example

The array is '[8, 4, 5, 3]'

1. Starting with the first element of the array '8', and then comparing it to the next element '4'. the two are swapped so now the array is [4, 8, etc].

2. Now step back and compare '3' with no previous element, continue forward.

3. Now compare and swap '8' with '5' swap them to get to [4, 5, 8, 3].

4. Once again compare and swap '8' with the next number in the array '3' giving us [4, 5, 3, 8].

5. The Gnome sorting algorithm will continue this sorting method until we are given or better, left with [3, 4, 5, 8].

## Performance

1. On average Gnome Sort takes quadratic time because each of the elements in the array may need take time to be compared and swapped. (Average Case: O(n2))
2. In the worst case scenario each element has to bve swapped in reverse order meaning multiple swaps on each of the elements (Worst Case: O(n2))
3. If the array is basically sorted this is the best case scenario as Gnome Sort performs best under this scenario due to a linear number of operations (Best Case: O(n))

## Efficency 

1. Gnome Sort, sorts the array as it is placed, meaning it requires no additional space to perform its task. Space Complexity O(1).
2. If Gnome sort encounters multiple elements of the same number it will maintain their place in respects to each other whiel sitll sorting them, meaning it maintains stability.

## Conclusion

Gnome Sort is a very simple and easy to use/implement sorting algorithm, but it will begin to lose effeciency in larger projects due to its quadratic time complexity in the average and worst case scenarios.

# Pancake Sort

Pancake sort is a sorting algorithm that iteratively sorts portions of arrays by flipping the elements to bring the largest unsorted element to its correct position.

1. The main operations of pancake sort is flipping. Flipping on a portion of an array in order to reverse its elements up to a specified location.

2. Pancake Sort Process

- Starting with the entire array of elements which need sorting.

- Iteratively find the largest number in the UN sorted array

- Perform the flipping operation on the largest element to the beginning of the unsorted portion.

- Once first flip is done, another is done to then put/sort the element into its correct position in the SORTED portion.

- Repeat afformentioned steps untl array is sorted.

3. Example

Array to be sorted = [7, 2, 4]

1. First sort

- Indetify the largest element in the array in its unsorted [(7) 2 4]

- flip the array to the last element (index) in the array [(4) 2 7]

- What the array should look like after the first pass [4 2 7]

2. Second Sort

- indetify the largest element in the remaining unsorted portion [(4) 2]

- flip the array to the last element (index) in the array [2 4]

- the algorithm is now sorted and the array should look like [2, 4, 7] 

## Performance and Effciency

- In the worst scenario, where n is the number of elements in the array. This is becasue the worst case scenario is each element requiring multiple flips to reach its correct position. Time Complexity O(n2)

- 