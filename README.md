# implement List.indexOf

`while`-style and recursive implementations at the top of
OrderedList_inArraySlots.java

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

y = log2(x) refers to the exponent required so that raising 2 to that exponent returns x

The graph of y = log2(x) is defined for x > 0. There is a vertical asymptote at x = 0, with the graph
going from negative infinity and increasing, passing through 0 at x = 1, and then
slowing down the growth significantly.


0. The problem is: given an ordered list of integers, find the index of a particular value.
1. The recursive abstraction is when asked to find a value in a list of size n, the recursive
abstraction finds the value in the correct half of the list with size n / 2.
2.  The if(low > high) is the decision between base or recursive cases.
    The return -2 is the solution to the base case
    The solution to the recursive cases:
      There is no combiner
      The recursive abstraction is the call to return indexOf_recursive( findMe , low, pageToCheck -1, false);
      There is no leftover.
