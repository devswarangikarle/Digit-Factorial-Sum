# Digit-Factorial-Sum

Sam is fascinated by factorials and decides to explore them in a unique way. Given an integer n, he wants to calculate the sum of the factorials of each digit in n. For any digit x, its factorial, x!, is the product of all positive integers from 1 to x. Can you help Sam find the sum of these factorials for each digit in n?

def digit_factorial_sum(n):
    # Precompute factorials for digits 0 to 9
    factorial = [1] * 10
    for i in range(2, 10):
        factorial[i] = factorial[i - 1] * i

    # Calculate the sum of the factorials of the digits
    sum_factorials = 0
    for digit in str(n):
        sum_factorials += factorial[int(digit)]

    return sum_factorials

# Input reading
n = int(input())
# Output result
print(digit_factorial_sum(n))
