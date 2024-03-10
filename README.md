# factorial-of-given-number
def factorial(n):
	if n < 0:
		return 0
	elif n == 0 or n == 1:
		return 1
	else:
		fact = 1
		while(n > 1):
			fact *= n
			n -= 1
		return fact

# Driver Code
num = 5
print("Factorial of",num,"is",
factorial(num))
# approach-2
# Function to find factorial of given number
def factorial(n):
	
	res = 1
	
	for i in range(2, n+1):
		res *= i
	return res
# Driver Code
num = 5
print("Factorial of", num, "is",
factorial(num))
# approach-3
# Python 3 program to find factorial
# of a given number using prime
# factorization method.

# Function to find prime factors of a number
def primeFactors(n):
	factors = {}
	i = 2
	while i*i <= n:
		while n % i == 0:
			if i not in factors:
				factors[i] = 0
			factors[i] += 1
			n //= i
		i += 1
	if n > 1:
		if n not in factors:
			factors[n] = 0
		factors[n] += 1
	return factors

# Function to find factorial of a number
def factorial(n):
	result = 1
	for i in range(2, n+1):
		factors = primeFactors(i)
		for p in factors:
			result *= p ** factors[p]
	return result

# Driver Code
num = 5
print("Factorial of", num, "is", factorial(num))


