---
layout: post
title:  "Sorting Algorithms"
categories: notes
tag: notes
---

Just a random note on sorting algorithms...

Here's a <a href="https://www.bigocheatsheet.com/?goback=.gde_98713_member_241501229">time/space complexity cheatsheet</a>.

## Insertion Sort

* **Time complexity:** O(N<sup>2</sup>)
* **Space complexity:** O(1)

* **Algorithm:** (to sort in ascending order)
    1. Iterate over the array.
    2. Compare the current element to its predecessor.
    3. If the predecessor is larger than the current element, swap them.
    4. Now repeat the same steps: compare the current element with its new predecessor, and swap them if needed.
    5. Repeat until the current element is at its right place.

<img src="/assets/images/insertion-sort.png" alt="insertion sort" style="width:300px; display:block; margin-left:auto; margin-right:auto;"/>

## Selection Sort

* **Time complexity:** O(N<sup>2</sup>)
* **Space complexity:** O(1)

* **Algorithm:** (to sort in ascending order)
    1. There will be 2 parts to the array: 1) the sorted part, and 2) the unsorted part.
    1. Iterate over the unsorted part of the array, find the minimum element there.
    2. Move the minimum element up into the sorted part of the array.

## Quick Sort

* **Time complexity:** O(N log N) [on average]
* **Space complexity:** O(log N) [on average]

* **Algorithm:** (to sort in ascending order)
    1. Pick an element as pivot, supposed pivot = x.
    2. Partition the given array around the pivot.
    3. Put all elements greater than x after x, and all elements smaller than x before x.
    4. Sort the two parts of the array (before x and after x) recursively.

<img src="/assets/images/quick-sort.png" alt="quick sort" style="width:550px; display:block; margin-left:auto; margin-right:auto;"/>

* **Why does quick sort take up extra memory?**

    There are two ways memory gets assigned: 1) implicitly, and 2) explicitly. Here, quicksort is an example of the implicit use of memory. When using quick sort, the function is called recursively O(N) times in the worst case and O(log N) times in the average case. Each recursive call takes O(1) space, so the space complexity of quick sort is O(N) in the worst case and O(log N) on average.

## Merge Sort

* **Time complexity:** O(N log N)
* **Space complexity:** O(N)

* **Algorithm:** (to sort in ascending order)
    1. Divide the array into two halves.
    2. Call the merge sort function on each of the two halves.
    3. Merge the two sorted halves.

<img src="/assets/images/merge-sort.png" alt="merge sort" style="width:550px; display:block; margin-left:auto; margin-right:auto;"/>

## Heap Sort

* **Time complexity:** O(N log N)
* **Space complexity:** O(1)

* **Algorithm:** (to sort in ascending order)
    1. Build a min-heap from the input array.
    2. Remove the root of the heap (smallest element) and place it into the output array. Adjust the remaining elements so that they still form a heap.
    3. Repeat the above step until the heap is empty. <br/><br/>

* **What is a heap?**

    The heap is a tree-based data structure, in which all nodes are greater than (or smaller than) their children. This is the **heap invariant**. Depending on the relation between each node and its children, the heap is referred to as either a **min-heap** or a **max-heap**.

* **How to implement a heap?**

    We can use an **array** to implement a heap. If the index of an element in the array is `i`, then its left child is at index `2i+1`, its right child is at index `2i+2`, and parent is at the lower bound of `(i-1)/2`.

* **How to build a heap from the input array?**
    
    The easiest way is to move a pointer down the input array, and make sure everything before the pointer forms a heap. In other words, as we move the pointer down the array, we are essentially adding new elements, one at a time, into the heap.

For a detailed description (with diagrams) of Heap Sort, see <a href="https://www.programiz.com/dsa/heap-sort">https://www.programiz.com/dsa/heap-sort</a>.

## Bubble Sort

* **Time complexity:** O(N<sub>2</sub>)
* **Space complexity:** O(1)

* **Algorithm:**
    1. Iterate through the array.
    2. Swap adjacent elements if they are in the wrong order.
    3. Repeat the above two steps. 
    4. Stop when a whole iteration is completed without any swaps.

<img src="/assets/images/bubble-sort.png" alt="bubble sort" style="width:500px; display:block; margin-left:auto; margin-right:auto;"/>

## Bucket Sort

Bucket sort is mainly useful when input is uniformly distributed across a range.

* **Time complexity:** O(N + k) [on average]
* **Space complexity:** O(N)

* **Algorithm:**
    1. Create n empty buckets.
    2. Insert each element into the corresponding bucket (see diagram below for an example).
    3. Sort each bucket.
    4. Concatenate all sorted buckets.

<img src="/assets/images/bucket-sort.png" alt="bucket sort" style="width:500px; display:block; margin-left:auto; margin-right:auto;"/>

## Counting Sort

Counting sort is useful when the input lies within a specific range.

* **Time complexity:** O(N + k), N = size of input, k = size of range
* **Space complexity:** O(k)

* **Algorithm:**
    1. Iterate throught the input array.
    2. Count the number of occurrences of each unique element in the array, and store this information in an auxiliary array.
    3. When this is done, iterate through the auxiliary array and print the values out.