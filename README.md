# Assignment     INDEX NUMBER: 10659106  
When does the worst case of Quicksort occur?
The answer depends on strategy for choosing pivot. In early versions of Quick Sort where leftmost (or rightmost) element is chosen as pivot, the worst occurs in following cases.
1) Array is already sorted in same order.
2) Array is already sorted in reverse order.
3) All elements are same (special case of case 1 and 2)
The worst case occurs when the partition process always picks greatest or smallest element as pivot. If we consider above partition strategy where last element is always picked as pivot, the worst case would occur when the array is already sorted in increasing or decreasing order. Following is recurrence for worst case.
Since these cases are very common use cases, the problem was easily solved by choosing either a random index for the pivot, choosing the middle index of the partition or (especially for longer partitions) choosing the median of the first, middle and last element of the partition for the pivot. With these modifications, the worst case of Quick sort has less chances to occur, but worst case can still occur 
if the input array is such that the maximum (or minimum) element is always chosen as pivot.


When does the best case of  Quicksort occur?
In the most balanced case, each time we perform a partition we divide the list into two nearly equal pieces. This means each recursive call processes a list of half the size. Consequently, we can make only log2 n nested calls before we reach a list of size 1. This means that the depth of the call tree is log2 n. But no two calls at the same level of the call tree process the same part of the original list; thus, each level of calls needs only O(n) time all together (each call has some constant overhead, but since there are only O(n) calls at each level, this is subsumed in the O(n) factor). The result is that the algorithm uses only O(n log n) time.


Analysis of QuickSort(WorstCase) T(n) ∈ Ω(n
2)
When quicksort always has the most unbalanced partitions possible, then the original call takes cncnc, n time for some constant ccc, the recursive call on n-1n−1n, minus, 1 elements takes c(n-1)c(n−1)c, left parenthesis, n, minus, 1, right parenthesis time, the recursive call on n-2n−2n, minus, 2 elements takes c(n-2)c(n−2)c, left parenthesis, n, minus, 2, right parenthesis time, and so on.
The worst-case choice: the pivot happens to be the largest (or
smallest) item.
• Then one subarray is always empty.
• The second subarray contains n − 1 elements, i.e. all the
elements other than the pivot.
• Quicksort is recursively called only on this second group.
However, quicksort is fast on the “randomly scattered” pivots.


Analysis of Quicksort(BestCase)
When quicksort always has the most unbalanced partitions possible, then the original call takes cncnc, n time for some constant ccc, the recursive call on n-1n−1n, minus, 1 elements takes c(n-1)c(n−1)c, left parenthesis, n, minus, 1, right parenthesis time, the recursive call on n-2n−2n, minus, 2 elements takes c(n-2)c(n−2)c, left parenthesis, n, minus, 2, right parenthesis time, and so on

 
