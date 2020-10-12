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

c)  def bunnyEars(bunnies):
      if bunnies == 0:              O(1)
        return 0                    O(1)

      return 2 + bunnyEars(bunnies-1)   O(n/2)

ANSWER: O(n)
COMMENTS: The recursive component reduces n by one-half, but that is the same as saying the complexity is O(1/2 * n).  The constant is always removed so the complexity reduces to O(n).

## Exercise II

My understanding of the problem is that we are solving for f, which is the lowest level floor at which the eggs will break.  The function takes the number of floors in the building as a parameter and should return f, or the lowest floor at which the eggs will break.

To solve the problem, we should start at floor one and drop an egg.  If the egg breaks, we return the floor beneath it, which would be zero. If the egg does not break, we go up a floor and try again. The exercise is stopped whenever an egg breaks, and we will return the floor beneath it.

Pseudocode would be something like:

iterate up the floors starting at one
drop the egg and see if it breaks
if it breaks, stop and return f -1 
if it does not break, increment f by one and try again.
