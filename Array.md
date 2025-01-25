# Array

## 1.  Permutations 46
- Given an array nums of distinct integers, return all the possible permutations . You can return the answer in any order.

  ```
  Example 1:
     Input: nums = [1,2,3]
     Output: [[1,2,3],[1,3,2],[2,1,3],[2,3,1],[3,1,2],[3,2,1]]

- Solution
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

- Solution
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


- Solution
   -  Use Set Then check the sequence.

