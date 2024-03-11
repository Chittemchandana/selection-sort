# selection-sort
# Selection Sort Algorithm
# SELECTION SORT(arr, n)  
# Step 1: Repeat Steps 2 and 3 for i = 0 to n-1  
# Step 2: CALL SMALLEST(arr, i, n, pos)  
# Step 3: SWAP arr[i] with arr[pos]  [END OF LOOP]  
# Step 4: EXIT  
# approach1
public void selectionSort(int[] arr) {
    int n = arr.length;

    for (int i = 0; i < n - 1; i++) {
        int minIndex = i;

        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIndex]) {
                minIndex = j;
            }
        }

        // swap arr[minIndex] and arr[i]
        int temp = arr[minIndex];
        arr[minIndex] = arr[i];
        arr[i] = temp;
    }
}

# approach2
# Python program for implementation of Selection 
# Sort 
import sys 
A = [64, 25, 12, 22, 11] 

# Traverse through all array elements 
for i in range(len(A)): 
	
	# Find the minimum element in remaining 
	# unsorted array 
	min_idx = i 
	for j in range(i+1, len(A)): 
		if A[min_idx] > A[j]: 
			min_idx = j 
			
	# Swap the found minimum element with 
	# the first element		 
	A[i], A[min_idx] = A[min_idx], A[i] 

# Driver code to test above 
print ("Sorted array") 
for i in range(len(A)): 
	print("%d" %A[i],end=" , ") 
# o/p:Sorted array: 11 12 22 25 64 

