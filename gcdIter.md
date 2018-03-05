<center><h1>GCD Iter</h1></center>

#### Discription:
```markdown
input two integers a and b
output the gcd of a and b
```

### gcdIter.cpp
```markdown
#include <iostream>

using namespace std;

int gcd(int a, int b) {
  while(a %= b) swap(a, b);
  return b;
}

int main()
{
  int a, b;
  cin >> a >> b;
  cout << gcd(a, b) << endl;
}
```

### gcdIter.c
```markdown
#include <stdio.h>

int gcd(int a, int b) {
  while(a %= b) swap(a, b);
  return b;
}

int main()
{
  int a, b;
  scanf("%d%d", &a, &b);
  printf("%d\n", gcd(a, b));
}
```
