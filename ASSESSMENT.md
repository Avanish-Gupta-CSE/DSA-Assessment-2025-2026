# DSA & Software Engineering Assessment
**Date:** November 19, 2025  
**Estimated Time:** 4-6 hours (spread across 2-3 days)

---

## Instructions

1. **Be Honest:** This assessment helps identify your current level—there are no wrong answers
2. **Don't Look Up Solutions:** Write your first instinct and approach
3. **If Stuck:** Explain WHERE and WHY you're stuck—that's valuable information
4. **Time Limits:** Don't spend more than 20 minutes on any single coding problem
5. **Language:** Use C++ or JavaScript/TypeScript (your choice, can mix)
6. **Format:** Create separate files for each part as per folder structure

---

## PART 1: Conceptual Understanding (30 minutes)
**File:** `Part1-Conceptual/answers.md`

### 1.1 Data Structures Fundamentals

**Q1:** Imagine you're building a browser's "Back" button functionality (going to previous pages). Which data structure would you use and why? What if you also needed a "Forward" button?

**Q2:** You need to store 1 million user records where you frequently need to check "Does user with email X exist?" What data structure would you choose and why? What's the approximate time complexity?

**Q3:** In your own words, explain the difference between:
- Array vs Linked List (when would you choose one over the other?)
- Stack vs Queue (give a real-world example of each)

**Q4:** You have a social network where you need to find if Person A is connected to Person B (directly or through mutual friends). What data structure represents this problem?

### 1.2 Time/Space Complexity

**Q5:** Analyze this code and tell me the time complexity:
```cpp
for(int i = 0; i < n; i++) {
    for(int j = i; j < n; j++) {
        cout << i + j << endl;
    }
}
```

**Q6:** Why is Binary Search O(log n) and not O(n)? Explain in simple terms.

**Q7:** If an algorithm uses O(n) space, what does that mean in practical terms?

---

## PART 2: Code Reading & Debugging (20 minutes)
**File:** `Part2-Code-Reading/analysis.md`

**2.1** What does this function do? Explain the logic step by step:
```cpp
int mystery(vector<int>& arr) {
    int maxSum = arr[0];
    int currentSum = arr[0];
    
    for(int i = 1; i < arr.size(); i++) {
        currentSum = max(arr[i], currentSum + arr[i]);
        maxSum = max(maxSum, currentSum);
    }
    
    return maxSum;
}
```

**2.2** This code has a bug. Find it and explain what's wrong:
```cpp
int findElement(vector<int>& arr, int target) {
    int left = 0, right = arr.size();
    
    while(left < right) {
        int mid = (left + right) / 2;
        
        if(arr[mid] == target) return mid;
        else if(arr[mid] < target) left = mid;
        else right = mid;
    }
    
    return -1;
}
```

---

## PART 3: Basic Problem Solving (45-60 minutes)
**Files:** Create separate `.cpp` or `.js` files for each problem

### Problem 3.1: Array Product (Easy-Medium)
**File:** `Part3-Basic-Problems/problem1-array-product.cpp`

```
Given an array of integers, return a new array where each element 
is the product of all elements except itself.

Example:
Input: [1, 2, 3, 4]
Output: [24, 12, 8, 6]
Explanation: 
- arr[0] = 2 * 3 * 4 = 24
- arr[1] = 1 * 3 * 4 = 12
- arr[2] = 1 * 2 * 4 = 8
- arr[3] = 1 * 2 * 3 = 6

Constraint: Do it WITHOUT using division operator

Your task:
1. Write your approach/algorithm first (as comments)
2. Implement the solution
3. Analyze time and space complexity
```

### Problem 3.2: Two Sum in Sorted Array (Easy-Medium)
**File:** `Part3-Basic-Problems/problem2-two-sum.cpp`

```
Given a sorted array and a target sum, find two numbers that add up 
to the target. Return their indices.

Example:
Input: arr = [2, 7, 11, 15], target = 9
Output: [0, 1] (because arr[0] + arr[1] = 2 + 7 = 9)

Follow-up: Can you do it in O(n) time?

Your task:
1. Write brute force approach first
2. Then write optimized O(n) solution
3. Compare both approaches
```

### Problem 3.3: Anagram Checker (Easy)
**File:** `Part3-Basic-Problems/problem3-anagram.cpp`

```
Check if two strings are anagrams of each other.

Example 1:
Input: s1 = "listen", s2 = "silent"
Output: true

Example 2:
Input: s1 = "hello", s2 = "world"
Output: false

Your task:
1. Implement the solution
2. What's the time complexity?
3. What's the space complexity?
```

---

## PART 4: Intermediate Concepts (40-50 minutes)

### 4.1: Recursion Understanding
**File:** `Part4-Intermediate/recursion-analysis.md`

Without coding, analyze this recursive function:

```cpp
int solve(int n) {
    if(n <= 1) return n;
    return solve(n-1) + solve(n-2);
}
```

Questions:
1. What does this function calculate?
2. What's the time complexity of this implementation?
3. What's the problem with this implementation?
4. How would you optimize it? (Explain the approach)

### 4.2: Sorting Strategy
**File:** `Part4-Intermediate/sorting-strategy.md`

```
You have an array that's "almost sorted" - each element is at most 
k positions away from its correct sorted position.

Example: If k=2, an element at index 5 in the sorted array could be 
at index 3, 4, 5, 6, or 7 in the given array.

Question: Which sorting algorithm would be most efficient here and why?
(You don't need to code it, just explain your reasoning)
```

### 4.3: Sliding Window Problem
**File:** `Part4-Intermediate/sliding-window.cpp`

```
Given an array of positive integers and a number k, find the 
maximum sum of any contiguous subarray of size k.

Example:
Input: arr = [2, 1, 5, 1, 3, 2], k = 3
Output: 9 
Explanation: Maximum sum subarray is [5, 1, 3] = 9

Your task:
1. Write your initial approach
2. If stuck, write down:
   - What you tried
   - Where you got stuck
   - What you think might work
3. Implement if you can solve it
```

---

## PART 5: Advanced Topics - Quick Check (15-20 minutes)
**File:** `Part5-Advanced/answers.md`

### 5.1 Binary Search Trees
```
In a Binary Search Tree (BST), you need to find if a value exists.

Questions:
1. Explain the approach you'd use
2. What's the average time complexity?
3. What's the worst-case time complexity?
4. When would the worst case occur?
```

### 5.2 Graph Traversal
```
You have a maze represented as a 2D grid:
- 0 = path you can walk on
- 1 = wall you cannot cross
- S = start position
- E = end position

Question: How would you find if there's a path from S to E?
(Conceptual answer - which algorithm/approach would you use and why?)
```

### 5.3 Dynamic Programming
```
Question: What is the difference between Memoization and Tabulation in DP?

If you're not familiar with this yet, write:
"Not familiar with this yet - will learn in Week 12"
```

---

## PART 6: System Design Basics (15-20 minutes)
**File:** `Part6-System-Design/design-notes.md`

### 6.1 URL Shortener Design

```
Design a simple URL shortener service (like bit.ly).

Answer these questions:
1. How would you generate short URLs from long URLs?
2. How would you store the mapping between short and long URLs?
3. What database would you use (SQL or NoSQL) and why?
4. How would you handle millions of requests per day?

(Just give your thought process - no single right answer)
```

### 6.2 Database Choice

```
Question: What's the difference between SQL and NoSQL databases? 
When would you choose one over the other?

Give real-world examples from your experience at Berkadia or 
STMicroelectronics if possible.
```

---

## PART 7: OOP Quick Check (10-15 minutes)
**File:** `Part7-OOP/oops-concepts.md`

### 7.1 OOP Principles

Explain these OOP concepts with a real-world example:

1. **Encapsulation:** 
2. **Polymorphism:** 
3. **Inheritance:** 
4. **Abstraction:** 

### 7.2 SOLID Principles

```
Question: What are the SOLID principles?

List what you remember. If you don't remember all 5, that's okay - 
just list what you know and we'll cover the rest during preparation.
```

### 7.3 Design Patterns (Bonus)

```
Do you know any design patterns? If yes, name a few and explain 
when you'd use them.

If not familiar, write: "Will learn during LLD preparation"
```

---

## Submission Guidelines

### How to Submit

1. **Create folders** as per the structure in README.md
2. **Add your solutions** in respective files
3. **Commit and push** to GitHub:
   ```bash
   git add .
   git commit -m "Complete Part 1-3 of assessment"
   git push origin main
   ```
4. **Share the repo link** (you already did this!)

### What to Include

For each problem:
- ✅ Your approach/thought process (even if incomplete)
- ✅ Working code (C++ or JS/TS)
- ✅ Time and space complexity analysis
- ✅ If stuck: explain where and why

For conceptual questions:
- ✅ Your understanding in your own words
- ✅ Real-world examples if possible
- ✅ Honest "I don't know" if applicable

---

## Timeline

**Day 1 (Nov 19-21):** Parts 1-3  
**Day 2 (Nov 22-24):** Parts 4-5  
**Day 3 (Nov 24-25):** Parts 6-7  

**By Nov 25:** Complete assessment, ready for feedback and roadmap!

---

## Important Reminders

- This is NOT a test—it's a diagnostic tool
- Every "I don't know" helps me help you better
- Focus on understanding, not perfection
- We'll fill all gaps together over 16 weeks

---

**Ready? Let's begin your transformation journey! 💪**