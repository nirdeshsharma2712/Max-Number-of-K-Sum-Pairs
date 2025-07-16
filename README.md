# 📊 LeetCode Problem: Max Number of K-Sum Pairs

## 🧩 Problem Statement

You are given an **integer array** `nums` and an integer `k`.
Return the **maximum** number of operations you can perform on the **array**.

> **Note :**
> - In one operation, you can pick **two numbers** from the array **whose sum** equals `k` and remove them from the array.



## 🧠 Approach: Two Pointers After Sorting

- **Sort** the array to bring potential pairs together.

- Use two pointers: `i` at start, `j` at end.

- While `i < j`:
> - If `nums[i] + nums[j] == k` → `count++`, move both pointers.
> - If `sum > k` → move `j--`
> - If `sum < k` → move `i++`



## ✅ Example Walkthrough

### Example 1

##### Input: nums = [1,2,3,4], k = 5
##### Output: 2

##### Explanation: 
<pre> Starting with nums = [1,2,3,4]:
  
- Remove numbers 1 and 4, then nums = [2,3] <br>
- Remove numbers 2 and 3, then nums = [] <br>
There are no more pairs that sum up to 5, hence a total of 2 operations.
  
</pre>

### Example 2

##### Input: nums = [3,1,3,4,3], k = 6
##### Output: 1

##### Explanation: 
<pre> Starting with nums = [3,1,3,4,3]:
  
- Remove the first two 3's, then nums = [1,4,3]<br>
There are no more pairs that sum up to 6, hence a total of 1 operation.
  
</pre>


## 🛠️ Constraints

- `1 <= nums.length <= 10^5`
- `1 <= nums[i] <= 10^9`
- `1 <= k <= 10^9`
