<center><h1>Sum Of Numbers</h1></center>

#### Discription:
```cpp
input n and then n integers
output the sum of the n numbers
```

### sumOfNumbers.cpp
```cpp
#include <iostream>

using namespace std;

int main()
{
  int n, tmp, sum = 0;
  cin >> n;
  for(int i=0;i<n;i++) {
    cin >> tmp;
    sum += tmp;
  }
  cout << sum << endl;
}
```

### sumOfNumbers.c
```c
#include <stdio.h>

int main()
{
  int n, tmp, sum = 0;
  scanf("%d", &n);
  int i;
  for(i=0;i<n;i++) {
    scanf("%d", &tmp);
    sum += tmp;
  }
  printf("%d", sum);
}
```
