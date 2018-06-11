<center><h1>Max of three numbers</h1></center>

#### Discription:
```cpp
input three integers
output the max value among the three numbers
```

### maxOfThreeNumbers.cpp
```cpp
#include <iostream>

using namespace std;

int maxOfThreeNumbers(int a, int b, int c) {
  if(a > b && a > c) return a;
  if(b > a && b > c) return b;
  return c;
}

int main()
{
  int a, b, c;
  cin >> a >> b >> c;
  cout << maxOfThreeNumbers(a, b, c) << endl;
}
```

### maxOfThreeNumbers.c
```c
#include <stdio.h>

int maxOfThreeNumbers(int a, int b, int c) {
  if(a > b && a > c) return a;
  if(b > a && b > c) return b;
  return c;
}

int main()
{
  int a, b, c;
  scanf("%d%d%d", &a, &b, &c);
  printf("%d\n", maxOfThreeNumbers(a, b, c));
}
```
