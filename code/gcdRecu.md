<center><h1>GCD Recu</h1></center>

#### Discription:
```cpp
input two integers a and b
output the gcd of a and b
```

### gcdRecu.cpp
```cpp
#include <iostream>

using namespace std;

int gcd(int a, int b) {
  return a % b ? gcd(b, a%b) : b;
}

int main()
{
  int a, b;
  cin >> a >> b;
  cout << gcd(a, b) << endl;
}
```

### gcdRecu.c
```c
#include <stdio.h>

int gcd(int a, int b) {
  return a % b ? gcd(b, a%b) : b;
}

int main()
{
  int a, b;
  scanf("%d%d", &a, &b);
  printf("%d\n", gcd(a, b));
}
```
