---
title: leetcode-16  3Sum Closest
subtitle: Welcome 👋  this is the java version of solution for leetcode number 16

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
> **Problem Analysis**  
> Problem Link: [16. 3Sum Closest](https://leetcode.com/problems/3sum-closest/)  
> Problem Description: Find three numbers in an array such that their sum is closest to a target value. Return the sum of the three integers. If there are multiple solutions, return the sum closest to the target.  
> Solution Approach:  
- This problem requires us to find three numbers in the array whose sum is closest to the target value. The sum could be equal to the target, greater than the target, or less than the target.
- The brute force approach would involve three nested loops, with a time complexity of O(n^3) and space complexity of O(1).
- An optimized solution involves sorting the array first, then using a two-pointer approach, with a time complexity of O(n^2) and space complexity of O(1).
- Initially, we enumerate the first number, and then we use front and back pointers to enumerate the second and third numbers. This way, we can ensure that as the second number increases, the third number decreases, allowing us to find the number closest to the target. This number will definitely be greater than the target and closest to it. Then, the sum of the previous numbers must be the closest to the target and less than it. If this sum is smaller than the previous result, we update the result.
```java
class Solution {
    public int threeSumClosest(int[] nums, int target) {
        Arrays.sort(nums);
        int n = nums.length;
        int res = 0x3f3f3f3f;
        for(int i = 0;i<nums.length;i++){
            for(int j = i+1,k=nums.length-1;j<k;j++){
                while(j<k-1&&nums[i]+nums[j]+nums[k-1]>=target)k--;
                if(nums[i]+nums[j]+nums[k]==target) return target;
                int s = nums[i]+nums[j]+nums[k];
                if(s-target<Math.abs(res-target))res = s;
                if(j<k-1){
                    s = nums[i]+nums[j]+nums[k-1];
                    if( (target-s)<Math.abs(res-target)){
                    res = s;
                    }
                
                }
            }
        }
        return res;

    }
}
