PART 1: Conceptual Understanding (30 minutes)
File: Part1-Conceptual/answers.md

1.1 Data Structures Fundamentals
Q1: Imagine you're building a browser's "Back" button functionality (going to previous pages). Which data structure would you use and why? What if you also needed a "Forward" button?
Ans:
What I think we can use a simple variable, acting as some flag which will be boolean in nature and
on click of Forward and Back buttons, which will change it's value

Q2: You need to store 1 million user records where you frequently need to check "Does user with email X exist?" What data structure would you choose and why? What's the approximate time complexity?
Ans. HashMaps with username as key and email as value, I m not sure

Q3: In your own words, explain the difference between:

Array vs Linked List (when would you choose one over the other?)
Ans: Array are good when you need to index an elements faster so in case when we know theposition at which our data exits then Arrays can be preferred.
LL are good when we need dynamic memory allocatiob (but in arrays also we have this provision but I m not sure what else there could be)

Stack vs Queue (give a real-world example of each)
Q4: You have a social network where you need to find if Person A is connected to Person B (directly or through mutual friends). What data structure represents this problem?
Ans: I think in both and stack and queue we can use it for social network, 
but still I cant tell which one is better than the other.

1.2 Time/Space Complexity
Q5: Analyze this code and tell me the time complexity:

for(int i = 0; i < n; i++) {
    for(int j = i; j < n; j++) {
        cout << i + j << endl;
    }
}
Ans: O(n)
Q6: Why is Binary Search O(log n) and not O(n)? Explain in simple terms.
Ans: because every time search space gets halved so it's like 1 + 1/2 + 1/4 + 1/8 + ....

Q7: If an algorithm uses O(n) space, what does that mean in practical terms?
Ans: Means with change in size of input the time taken will increase linearly.
