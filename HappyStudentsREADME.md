# leet-day70

# Problem Description
You are given a list of students represented by an integer array `nums`. The goal is to select a group of students in a way that makes them happy according to certain conditions. Each student has a value associated with them, and a student will be happy if one of the following two conditions is met:
1. The student is selected, and the total number of selected students is strictly greater than the value associated with that student.
2. The student is not selected, and the total number of selected students is strictly less than the value associated with that student.

The task is to find the number of ways to select students such that everyone remains happy.

# Approach
1. Sort the `nums` array in ascending order. Sorting the array allows us to process the students' values in an organized manner.

2. Initialize a variable `ans` to keep track of the count of ways to select students.

3. Handle three specific cases:
   - If no student is selected, then the student with the least value should be greater than 0.
   - For each student with index `i`, if `i+1` students are selected, then the student with the least value among the unselected students should be greater than `i+1`, and the student with the highest value among the selected students should be less than `i+1`.
   - If every student is selected, then the student with the highest value should be less than the total number of students.

4. Increment `ans` for each condition that is met.

5. Return `ans` as the final result, representing the number of ways to make the students happy.

# Complexity Analysis
- Time Complexity: The time complexity of this solution is O(n * log(n)), where `n` is the number of students. This is due to the sorting operation.
- Space Complexity: The space complexity is O(1) since we are using a constant amount of extra space for variables.

# How to Use
1. Define an instance of the `Solution` class.
2. Call the `countWays` function with the `nums` array as an argument.
3. The function will return the count of ways to make the students happy.

# Example
```cpp
vector<int> nums = {6, 0, 3, 3, 6, 7, 2, 7};
int result = Solution().countWays(nums);
cout << "Number of ways to make students happy: " << result << endl;
```

