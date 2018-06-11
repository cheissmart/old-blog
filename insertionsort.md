<center><h1>Insertion Sort</h1></center>

#### Discription:
```cpp
Insertion sort is a simple sorting algorithm that builds the final 
sorted array (or list) one item at a time. It is much less efficient
on large lists than more advanced algorithms such as quicksort, 
heapsort, or merge sort. 

Best Case：Ο(1)
當資料的順序恰好為由小到大時，每回合只需比較1次
Worst Case：Ο(n2)
當資料的順序恰好為由大到小時，第i回合需比i次
Average Case：Ο(n2)
第n筆資料，平均比較n/2次

```
[Insertion Sort Wiki](https://en.wikipedia.org/wiki/Insertion_sort)

### Insertion_sort.cpp
```cpp
#include <iostream>

using namespace std;

void insertion_sort(int* a, int n) {
  for(int i = 1; i < n; i++){
    int val = a[i], j;
    for(j = i-1; j>=0 && val<a[j]; j--) a[j+1] = a[j];
    a[j+1] = val;
  }
}


int main()
{
  int n, a[10000];
  cin >> n;
  for(int i=0;i<n;i++) cin >> a[i];
  insertion_sort(a, n);
  for(int i=0;i<n;i++) cout << a[i] << " ";
  cout << endl;
}
```
