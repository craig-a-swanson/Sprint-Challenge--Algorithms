#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)  a = 0                           O(1)
    while (a < n * n * n):          O(n)
      a = a + n * n                 O(1)

ANSWER: O(n)
COMMENTS: The while loop will iterate from zero to n-cubed, however 'a' is being incremented by n-squared. Therefore the time complexity an order of n.

b)  sum = 0                         O(1)
    for i in range(n):              O(n)
      j = 1                         O(1)
      while j < n:                  O(logn)
        j *= 2                      O(1)
        sum += 1                    O(1)

ANSWER: O(nlogn)
COMMENTS: The for loop is itereating from i to n, so the complexity is of Order(n). The sub-loop while statement is iterating from j to n but j is doubling with each iteration. This should be equivilent to logn. So the entire function simplifies to O(nlogn)

c)

## Exercise II


