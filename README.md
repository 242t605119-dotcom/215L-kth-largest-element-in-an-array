# LeetCode 215 - Kth Largest Element in an Array

## Problem Description

Given an integer array `nums` and an integer `k`, return the `k`th largest element in the array.

The array does not need to be sorted completely.

## Example

Input:

nums = [3,2,1,5,6,4]
k = 2

The sorted order is:

[6,5,4,3,2,1]

The 2nd largest element is `5`.

Output:

5

## Approach

We use a **Min Heap** of size `k`.

The heap stores the `k` largest elements seen so far.

For every number in the array:

- Add it to the heap.
- If the heap contains more than `k` elements, remove the smallest element.

After processing all elements, the smallest element in the heap is the `k`th largest element.

This avoids sorting the entire array.

## Algorithm

1. Create an empty min heap.
2. Add each number to the heap.
3. If the heap size becomes greater than `k`, remove the smallest value.
4. Continue until all numbers are processed.
5. Return the smallest value in the heap.

## Time Complexity

**O(n log k)**

Each element is added to the heap and may require a heap operation.

## Space Complexity

**O(k)**

The heap stores at most `k` elements.

## Key Concepts

- Heap
- Priority Queue
- Min Heap
- Arrays
- Kth Largest Element

## Author

T.nandhini
