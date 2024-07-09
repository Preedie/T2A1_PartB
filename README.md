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

- Due to Pancake being a being a in-place sorting algorithm no extra space is required to for it to operate, meaning it can operate on the array where it is rather than "needing space". Space Complexity O(1).

# Comparison

## Time Complexity

- Both of these sorting algorithms share the same space effciency O(1) due to using the operate in-place.  (they perform their sorting operations on the array so no extra space is required).

- Both algorithms use quadratic time complexity in the average to worst case scenarios (O(n^2)). This makes them inefficient for large projects or datasets compared to more efficient algorithms like quicksort or mergesort which can achieve O(n log n) time complexity in the average case scenario.

- While both algorithms are easy to implement and understand they have performance limitations when operating in worst case scenarios (especially) which will restrict them being very useful in a large dataset situation where other, quicker, sorting alorgorithms would be more useful.

- The application these particular sorting algorithms thrive in are simple in place sorting enviroments which minimal space and usage are being prioritized over the sorting speed or of course for educational purposes.

# Search Algorithms

## Dijkstra's Algorithm

Dijkstra's algorithm is used to find the shortest path from a sourcce node to all other nodes in a graph with weighted edges that are not negative.

### How it Works

1. Initialization

- the algorithm will start witha priority queue to keep track of the minimum distances from the source node to each other node on the graph.

- The distances will be initialized for all the nodes, except for the source node which is set to 0

2. Processing the nodes

- the smallest node in the priority queue is then extracted.

- Each node next to the extracted node will then be "measured" via their weights from the source node through the current node. If the distance is msaller than the previously known distances then the algorithm will update the distance and update the priority que.

3. Rinse and Repeat

- The above steps are then repeated until all the nodes have been processed OR until the priority que is empty.

4. Results

- after the algorithm is complete and ends, the shortest path distances from the source node to all other nodes will be known.

## Effeciency 

- When it comes to effciency dijkstra's algorthims time complexity will rely on the implementation of the priority que.

- The time complexity of Dijkstra's algorithm is O((V+E)logV), where 
V is the number of vertices and E is the number of edges.

- If a fibonacci heap is used the complexity can be reduced to O(VlogV+E).

# Linear Search

Linear search is a very simple searching algorithm that searches for a element  sequentially until the target element is found or all of the elements have been checked.

1. Interate the List

- Starting from the beginning of the list.

- Compare each element with the target element/value.

2. Comparison 

- if the current element matches the target element, the algorithm will return the targets index or depending on the context it will return TRUE.

- If the end of the list is reached without finding the target element then the return will be FALSE or -1.

## Effeciency 

- Linear Searches time complexity is O(n), where n is the number of elements in the list being searched.

- This means in the worst case scenario Linear Search may need to look at each element in the list to find the target element or work out if it does not exist in the list.

# Comparison of Dijkstra's Search and Linear Search Algorithms

1. Time Complexity

- Dijkstra due to its time complexity O((V+E)logV) using a binary heap, which is more effcient than Linear Searches O(n) complexity in most scenarions and especially so for large datasets.

As V and E grow, Dijkstra's algorithm can and is far faster than Linear Searches because Dijkstra's Algorithm processes the nodes based on their shortest path potential rather than checking over each node sequentially.

2. Suitability

- Dijkstra's algorithm is good for finding the sortest paths in graphs aslong as the weights are not negative.

- Linear Search Algorithm is good for unsorted lists where the exact location of a element is needed. (perhaps without a time constraint)

3. Data Structure Dependancy 

- Dijkstra's algorithm will require a graph structure and a priority queue (heap) for it to be effeciently implemented.

- Linear Search algorithm only requires a basic list or array.

# Conclusion

Ultimately, Dijkstra's algorithm is more efficient for its intended purpose which is finding the shortest paths in weighted graphs, aand this is especially so in larger datasets where effeciency matters. Linear Search as it is a simpler algorithm, it wil be less efficient for large lists compared to other specialized search algorithms like a binary search. Each of the algorithms serves a purposes which is dependant on the structure and of course the requirements of the data being processed.