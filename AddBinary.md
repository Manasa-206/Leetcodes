LeetCode #67 — Add Binary
Problem
Given two binary strings a and b, return their sum as a binary string.
Example 1
Input:
a = "11", b = "1"
Output:
"100"
Example 2
Input:
a = "1010", b = "1011"
Output:
"10101"
Approach
This problem is about adding binary numbers represented as strings.
Python provides built-in methods that make this process simple:
int(string, 2) → converts a binary string to an integer
bin(number) → converts an integer back to a binary string ('0b...' format)
So the strategy is:
Convert both binary strings to integers.
Add them.
Convert the sum back into binary.
Remove the "0b" prefix using [2:].
This approach is clean, readable, and uses Python’s strengths.
Code

class Solution(object):
    def addBinary(self, a, b):
        a_int = int(a, 2)  
        b_int = int(b, 2)  
        sum_int = a_int + b_int  
        return bin(sum_int)[2:]

⏱️ Complexity Analysis

Time Complexity: O(N)

N = max length of the strings a and b

Converting from binary string to integer is linear in length

Space Complexity: O(1)

Only constant extra space is used

🎯 Alternative Approach (Manual Binary Addition)

Another way is to implement binary addition manually:

iterate from right to left

maintain a carry

build output string bit by bit
