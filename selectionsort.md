<center><h1>Selection Sort</h1></center>

#### Discription:
```markdown
In computer science, selection sort is a sorting algorithm, 
specifically an in-place comparison sort. It has O(n2) time 
complexity, making it inefficient on large lists, and generally
performs worse than the similar insertion sort. Selection sort 
is noted for its simplicity, and it has performance advantages 
over more complicated algorithms in certain situations,
particularly where auxiliary memory is limited.

```
[Selection Sort Wiki](https://en.wikipedia.org/wiki/Selection_sort)

### Selection_sort.cpp
```markdown
#include <iostream>

using namespace std;

void selection_sort(int* a, int n) {
  for (int i = 0, minIndex; i < n - 1; i++) {
        minIndex = i;
        for (int j = i + 1; j < n; ++j)
            if (a[j] < a[minIndex]) minIndex = j;
        if (minIndex != i) swap(a[minIndex], a[i]);
    }
}


int main()
{
  int n, a[10000];
  cin >> n;
  for(int i=0;i<n;i++) cin >> a[i];
  selection_sort(a, n);
  for(int i=0;i<n;i++) cout << a[i] << " ";
  cout << endl;
}
```
