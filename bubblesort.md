<center><h1>Bubble Sort</h1></center>

#### Discription:
```markdown
Bubble sort, sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through 
thelist to be sorted, compares each pair of adjacent items and swaps them if they are in the wrong order. The 
pass through the list is repeated until no swaps are needed, which indicates that the list is sorted. The 
algorithm, which is a comparison sort, is named for the way smaller or larger elements "bubble" to the top of 
the list.

#Performance
Bubble sort has worst-case and average complexity both О(n2)
```
[Bubble Sort Wiki](https://en.wikipedia.org/wiki/Bubble_sort)

### Bubble_sort.cpp
```markdown
#include <iostream>

using namespace std;

void bubble_sort(int* a, int n) {
  for(int i=n-1;i>=0;i--) {
    for(int j=0;j<i;j++) {
      if(a[j] > a[j+1]) swap(a[j], a[j+1]);
    }
  }
}

int main()
{
  int n, a[10000];
  cin >> n;
  for(int i=0;i<n;i++) cin >> a[i];
  bubble_sort(a, n);
  for(int i=0;i<n;i++) cout << a[i] << " ";
  cout << endl;
}
```
