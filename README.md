# sum-of-bitwise-AND-of-all-subarrays
 find sum of bitwise AND of all subarrays 



Given an array consisting of N positive integers, find the sum of bit-wise and of all possible sub-arrays of the array.





For the sake of better understanding, let’s assume that any bit of an element is represented by the variable ‘i’ and the variable ‘sum’ is used to store the final sum.

The idea here is, we will try to find the number of AND values(sub-arrays with bit-wise and(&)) with ith bit set. Let us suppose, there are ‘Si‘ number of sub-arrays with ith bit set. For, ith bit, sum can be updated as sum += (2i * S).

We will break the task to multiple steps. At each step, we will try to find the number of AND values with ith bit set. For this, we will simply iterate through the array and find the number of contiguous segments with ith bit set and there lengths. For, each such segment of length ‘l’, value of sum can be updated as sum += (2i * l * (l + 1))/2.

Since, for each bit, we are performing O(N) iterations, the time complexity of this approach will be O(N).
