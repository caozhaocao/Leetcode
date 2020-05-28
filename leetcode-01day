9. 回文数
判断一个整数是否是回文数。回文数是指正序（从左向右）和倒序（从右向左）读都是一样的整数。

示例 1:

输入: 121
输出: true
示例 2:

输入: -121
输出: false
解释: 从左向右读, 为 -121 。 从右向左读, 为 121- 。因此它不是一个回文数。
示例 3:

输入: 10
输出: false
解释: 从右向左读, 为 01 。因此它不是一个回文数。

python3-code:
class Solution:
    def isPalindrome(self, x: int) -> bool:
        lst = list(str(x))
        while len(lst) > 1:
            if lst.pop(0) != lst.pop():
                return  False
        return True

#testcase
s=Solution()
s.isPalindrome(1212)


866. 回文素数
求出大于或等于 N 的最小回文素数。

回顾一下，如果一个数大于 1，且其因数只有 1 和它自身，那么这个数是素数。

例如，2，3，5，7，11 以及 13 是素数。

回顾一下，如果一个数从左往右读与从右往左读是一样的，那么这个数是回文数。

例如，12321 是回文数。
python3-code:
class Solution(object):
    def primePalindrome(self, N):
        def is_prime(n):
            return n > 1 and all(n%d for d in range(2, int(n**.5) + 1))

        for length in range(1, 6):
            #Check for odd-length palindromes
            for root in range(10**(length - 1), 10**length):
                s = str(root)
                x = int(s + s[-2::-1]) #eg. s = '123' to x = int('12321')
                if x >= N and is_prime(x):
                    return x
                    #If we didn't check for even-length palindromes:
                    #return min(x, 11) if N <= 11 else x

            #Check for even-length palindromes
            for root in range(10**(length - 1), 10**length):
                s = str(root)
                x = int(s + s[-1::-1]) #eg. s = '123' to x = int('123321')
                if x >= N and is_prime(x):
                    return x
                    
#testcase
solution=Solution()
print(solution.primePalindrome(8))
