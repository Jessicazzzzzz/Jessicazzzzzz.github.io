---
title: leetcode-15 threeSum
subtitle: Welcome 👋  this is the java version of solution for leetcode number 15

# Summary for listings and search engines
summary: This algorithm utilizes the two-pointer approach with a time complexity of O(n^2) and space complexity of O(1).
# Link this post with a project
# projects: []

# Date published
# date: '2'

# Date updated


# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
#   focal_point: ''
#   placement: 2
#   preview_only: false

authors:
  - admin
  - Jess

tags:
  - easy

categories:
  - Leetcode
---
> Solution:
> This problem requires us to find three numbers whose sum equals 0. If we use the brute force approach, it would involve three nested loops with a time complexity of O(n^3). However, by utilizing the two-pointer technique, we can achieve a time complexity of O(n^2). 
> The first step is to sort the array, ensuring it is in ascending order. Then, we enumerate the first number and the second number. We can use the two-pointer algorithm. If the result is greater than or equal to 0, we decrement the pointer `k`. This helps in deduplication and finding `k`, as the result set should not contain duplicate values. Therefore, we also need to deduplicate `i` and `j`. If they are the same as the previous number, we can skip them to achieve deduplication.



```java
class Solution {
    public List<List<Integer>> threeSum(int[] nums) {
       List<List<Integer>> ans = new LinkedList<>();
       // sort array
       Arrays.sort(nums);
       for(int i = 0;i<nums.length;i++){
      //  remove duplicate i
        if(i>0 && nums[i-1]==nums[i]) continue;
         for(int j = i+1,k = nums.length-1;j<k;j++){
//   remove duplicate j,compare to the ahead num,if equal ,continue
            if(j>i+1 && nums[j-1]==nums[j]) continue;
//  j and k-1 don't meet , and the sum of three >=0 , that means k need to -1
            while(j<k-1 && nums[i]+nums[j]+nums[k-1]>=0)k--;
            if(nums[i]+nums[j]+nums[k]==0){
                List<Integer> z = new LinkedList<>();
                z.add(nums[i]);
                z.add(nums[j]);
                z.add(nums[k]);
                ans.add(z);
            }
         }
    
       }
            return ans;
    }
}


