# searchSortedRotatedArray

# Algorithm

Define a method rotateSortArray that takes an integer array arr and an integer target as parameters. This method will perform the search operation.

Initialize two pointers, left and right, to the start and end indices of the array, respectively.

While the left pointer is less than or equal to the right pointer, do the following steps:

a. Calculate the middle index mid using the formula left + (right - left) / 2 to avoid integer overflow.

b. Check if the middle element arr[mid] is equal to the target. If it is, return mid as the index of the target element.

c. Check if the left half of the array is sorted. Compare arr[left] with arr[mid]:

If arr[left] is less than or equal to arr[mid], it means the left half is sorted.

Check if the target is within the range of the left half. If the target is greater than or equal to arr[left] and less than arr[mid], update the right pointer to mid - 1 to search in the left half.

If the target is not within the range, update the left pointer to mid + 1 to search in the right half.

If arr[left] is greater than arr[mid], it means the right half is sorted.

Check if the target is within the range of the right half. If the target is greater than arr[mid] and less than or equal to arr[right], update the left pointer to mid + 1 to search in the right half.

If the target is not within the range, update the right pointer to mid - 1 to search in the left half.

If the target element is not found after the while loop, return -1 to indicate that the target is not present in the array.

The algorithm uses the concept of binary search to efficiently search for an element in a rotated and sorted array. By comparing elements and adjusting the pointers, it narrows down the search range until the target element is found or the search range is exhausted.
