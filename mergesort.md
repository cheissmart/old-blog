<center><h1>Merge Sort</h1></center>

#### Discription:
```cpp
Best Case: O(nlogn)
Worst Case: O(nlogn)
Average Case: O(nlogn)
```
[Merge Sort Wiki](https://en.wikipedia.org/wiki/Merge_sort)

### merge_sort.cpp
```cpp
#include <bits/stdc++.h>

using namespace std;

void mergeSort(int *arr, int low, int high) {
    if (low < high) {
        int mid = (low + high) / 2;
         
        mergeSort(arr, low, mid);
        mergeSort(arr, mid + 1, high);
        merge(arr, low, mid, high);
    }
}
 
void merge(int *arr, int low, int mid, int high) {
    int leftIndex = low;
    int rightIndex = mid + 1;
    int tempArrLength = high - low + 1;
    int tempArr[tempArrLength];
    int tempIndex = 0;
     
    while (leftIndex <= mid && rightIndex <= high) {
        if (arr[leftIndex] <= arr[rightIndex]) {
            tempArr[tempIndex] = arr[leftIndex];
            leftIndex++;
        }
        else {
            tempArr[tempIndex] = arr[rightIndex];
            rightIndex++;
        }
        tempIndex++;
    }
    if (leftIndex > mid) {
        while (rightIndex <= high) {
            tempArr[tempIndex] = arr[rightIndex];
            rightIndex++;
            tempIndex++;
        }
    }
    else {
        while (leftIndex <= mid) {
            tempArr[tempIndex] = arr[leftIndex];
            leftIndex++;
            tempIndex++;
        }
    }
    leftIndex = low;
    for (tempIndex=0; tempIndex<tempArrLength; tempIndex++) {
        arr[leftIndex] = tempArr[tempIndex];
        leftIndex++;
    }
}
int main()
{
  int n, a[10000];
  cin >> n;
  for(int i=0;i<n;i++) cin >> a[i];
  mergeSort(a, 0, n - 1);
  for(int i=0;i<n;i++) cout << a[i] << " ";
  cout << endl;
}
```
