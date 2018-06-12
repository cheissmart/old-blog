<center><h1>Quick Sort</h1></center>

#### Discription:
```cpp
Best Case: O(nlogn)
Worst Case: O(n^2)
Average Case: O(nlogn)
```
[Quick Sort Wiki](https://en.wikipedia.org/wiki/Quicksort)

### quick_sort.cpp
```cpp
#include <iostream>

using namespace std;

void quicksort(int *data, int left, int right)
{
    int pivot, i, j;
    if (left >= right)
        return;
    pivot = data[left];
    i = left + 1;
    j = right;
    while (1) {
        while (i <= right) {
            if (data[i] > pivot) 
                break;
            i++;
        }
        while (j > left) {
            if (data[j] < pivot)
                break;
            j--;      
        }
        if (i > j)
            break;

        swap(&data[i], &data[j]);                                               }
    swap(&data[left], &data[j]);
    quicksort(data, left, j - 1);
    quicksort(data, j + 1, right);
}

int main()
{
  int n, a[10000];
  cin >> n;
  for(int i=0;i<n;i++) cin >> a[i];
  quick_sort(a, 0, n - 1);
  for(int i=0;i<n;i++) cout << a[i] << " ";
  cout << endl;
}
```
