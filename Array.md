# Array

## 1.  Permutations 46
  - Given an array nums of distinct integers, return all the possible permutations . You can return the answer in any order.

    ```
    Example 1:
      Input: nums = [1,2,3]
      Output: [[1,2,3],[1,3,2],[2,1,3],[2,3,1],[3,1,2],[3,2,1]]

  - ### Solution
      Using Recursion,  loop over every element and call the function repeatedly.



## 2. Next Permutation 31.
  - The next permutation of an array of integers is the next lexicographically greater permutation of its integer. 
    - For example, the next permutation of arr = [1,2,3] is [1,3,2].
    - Similarly, the next permutation of arr = [2,3,1] is [3,1,2].
    - While the next permutation of arr = [3,2,1] is [1,2,3] because [3,2,1] does not have a lexicographical larger rearrangement.

    ```
    Example 1:
      Input: nums = [1,2,3]
      Output: [1,3,2]

  - ### Solution
      - Intuition ye hai ki pehle vo element dhundhna hai jisse swap krna hai fir jisko krna hai or baki array sorted hoga to usko reverse krdena hai closest bnane ke liye.
      - Find the element `X` from behind i.e < i+1 
      - If no such element then reverse the array 
      - else find smallest element i.e >  `X` (from behind to X) and swap with that element 
      - Then reverse the array from `X` to end


## 3.  Longest Consecutive Sequence 128.
  - Given an unsorted array of integers nums, return the length of the longest consecutive elements sequence.

    ```
    Example 1:
    Input: nums = [100,4,200,1,3,2]
    Output: 4 
    Explanation: The longest consecutive elements sequence is [1, 2, 3, 4]. Therefore its length is 4.


  - ### Solution
    -  Use Set Then check the sequence.


## 4. Set Matrix Zeroes 73.
  - Given an `m x n` integer matrix `matrix`, if an element is `0`, set its entire row and column to `0`'s.

    You must do it in place.

    ### Example 1:
      ```
      Input: matrix = [[1,1,1],
                      [1,0,1],
                      [1,1,1]]
      ```
      ```
      Output: [[1,0,1],
              [0,0,0],
              [1,0,1]]
      ```

  - ### Solution
    -  Use a row array and column array to track which one has a 0 and fill it with 0 then again iterate and if these array contains 0 then make changes in array
    - Use first row and column to not use extra space

## 5. Rotate Image 48.
  - You are given an n x n 2D matrix representing an image, rotate the image by 90 degrees (clockwise).

  - You have to rotate the image in-place, which means you have to modify the input 2D matrix directly. DO NOT allocate another 2D matrix and do the rotation.

    ### Example 1:
      ```
      Input: matrix = [[1,2,3],
                       [4,5,6],
                       [7,8,9]]
      ```
      ```
      Output: [[7,4,1],
               [8,5,2],
               [9,6,3]]
      ```

  - ### Solution
    -  Transpose the matrix and reverse it 
    - Alternative, swap top with bottom then transpose

## 6. Spiral Matrix 54.
  - Given an m x n matrix, return all elements of the matrix in spiral order.


    ### Example 1:
       ```
      Input: matrix = [[1,2,3],
                      [4,5,6],
                      [7,8,9]]
      ```
      ```
      Output: [1,2,3,6,9,8,7,4,5]
      ```

  - ### Solution
    -  Make the logic for traversal in all directions ( top left bottom right)



## 7. Subarray Sum Equals K 560.
  - Given an array of integers nums and an integer k, return the total number of subarrays whose sum equals to k.

  - A subarray is a contiguous non-empty sequence of elements within an array.
 

    ### Example 1:
       ```
      Input: nums = [1,1,1], k = 2
      Output: 2
      ```
      

  - ### Solution
    -  Make the logic for prefix sum and store it in a map



## 8. Majority Element II 229.
  - Given an integer array of size n, find all elements that appear more than ⌊ n/3 ⌋ times.

    ### Example 1:
       ```
      Input: nums = [3,2,3]
      Output: [3]
      ```
      

  - ### Solution
    -  Moore's voting algorithm (extended version) take 4 pointers two for count and 2 for elements as there can only be a max of two elements 

## 9. 3Sum  15.
  - Given an integer array nums, return all the triplets `[nums[i], nums[j], nums[k]] `such that `i != j`, `i != k`, and `j != k`, and `nums[i] + nums[j] + nums[k] == 0`.

  - Notice that the solution set must not contain duplicate triplets.
    ### Example 1:
       ```
      Input: nums = [3,2,3]
      Output: [3]
      ```
      

  - ### Solution
    -  sort and fix one element and use two pointer to get rest of the elements. update start and end accordingly 


## 10. 4Sum  18.
  - Given an array `nums` of `n` integers, return an array of all the unique quadruplets `[nums[a], nums[b], nums[c], nums[d]]` such that:

  - `0 <= a, b, c, d < n`
  - `a`, `b`, `c`, and `d` are distinct.
  - `nums[a] + nums[b] + nums[c] + nums[d] == target`

    ### Example 1:
       ```
      Input: nums = [1,0,-1,0,-2,2], target = 0
      Output: [[-2,-1,1,2],[-2,0,0,2],[-1,0,0,1]]
      ```
      

  - ### Solution
    -  fix one element and use 3Sum approach for the rest of the elements 


## 11. Merge Intervals 56.
  - Given an array of intervals where intervals[i] = [starti, endi], merge all overlapping intervals, and return an array of the non-overlapping intervals that cover all the intervals in the input.


    ### Example 1:
       ```
      Input: intervals = [[1,3],[2,6],[8,10],[15,18]]
      Output: [[1,6],[8,10],[15,18]]
      Explanation: Since intervals [1,3] and [2,6] overlap, merge them into [1,6].
      ```
      

  - ### Solution
    -  sort the array and make a check on the array with the last added element on answer array. 


## 12. Reverse Pairs 493.
  - Given an integer array nums, return the number of reverse pairs in the array.
  - A reverse pair is a pair (i, j) where:
    - 0 <= i < j < nums.length and
    - nums[i] > 2 * nums[j].




    ### Example 1:
       ```
      Input: nums = [1,3,2,3,1]
      Output: 2
      Explanation: The reverse pairs are:
      (1, 4) --> nums[1] = 3, nums[4] = 1, 3 > 2 * 1
      (3, 4) --> nums[3] = 3, nums[4] = 1, 3 > 2 * 1
      ```
      

  - ### Solution
    -  apply merge sort and before merging use the logic for counting the possible pairs



## 13. Maximum Product Subarray 152.
  - Given an integer array nums, find a subarray that has the largest product, and return the product.

  - The test cases are generated so that the answer will fit in a 32-bit integer.
 
    ### Example 1:
       ```
      Input: nums = [2,3,-2,4]
      Output: 6
      Explanation: [2,3] has the largest product 6.
      ```
      

  - ### Solution
    -  produt form start and end of the array then return the max of both and answer



## 14 Search in Rotated Sorted Array 33.
  - Given an integer array arr of size N, sorted in ascending order (with distinct values) and a target value k. Now the array is rotated at some pivot point unknown to you. Find the index at which k is present and if k is not present return -1.

 
    ### Example 1:
       ```
      Input: nums = [4,5,6,7,0,1,2], target = 0
      Output: 4
      ```
      

  - ### Solution
    -  Use the fact that one side of the array will always be sorted and check on the sorted part if not present then eleminate that part else move pointers accordingly.



## 15. Find First and Last Position of Element in Sorted Array 34.
  - Given an array of integers nums sorted in non-decreasing order, find the starting and ending position of a given target value.
  - If target is not found in the array, return [-1, -1].

  - You must write an algorithm with O(log n) runtime complexity.
 
    ### Example 1:
       ```
      Input: nums = [5,7,7,8,8,10], target = 8
      Output: [3,4]
      ```
      

  - ### Solution
    -  Apply binary Search after getting the element find the first occurance and last occurance of the element.



## 16.  Search in Rotated Sorted Array 33.
  - Given an integer array arr of size N, sorted in ascending order (with distinct values) and a target value k. Now the array is rotated at some pivot point unknown to you. Find the index at which k is present and if k is not present return -1.
 
    ### Example 1:
       ```
      Input: nums = [4,5,6,7,0,1,2], target = 0
      Output: 4
      ```
      

  - ### Solution
    -  Left and Right will always be sorted so use this fact to move Start and End. 


## 17. Search in Rotated Sorted Array II 81.
  - Given an integer array arr of size N, sorted in ascending order (may contain duplicate values) and a target value k. Now the array is rotated at some pivot point unknown to you. Return True if k is present and otherwise, return False. 
 
    ### Example 1:
       ```
      Input: nums = [2,5,6,0,0,1,2], target = 0
      Output: true
      ```
      

  - ### Solution
    -  Left and Right will always be sorted so use this fact to move Start and End. Handle the one edge case where nums at (start = end = mid) then just move start and end by one place and continue. 







