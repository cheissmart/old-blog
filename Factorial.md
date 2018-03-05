<center><h1>Factorial</h1></center>

#### Discription:
```markdown
input an integer n
output n!
(n! = 1 x 2 x 3 x ... x n)
```

### Factorial.cpp
```markdown
#include <iostream>

using namespace std;

int main()
{
  int n, ans = 1;
  cin >> n;
  for(int i=1;i<=n;i++) ans *= i;
  cout << ans << endl;
}
```

### Factorial.c
```markdown
#include <stdio.h>

int main()
{
  int n, ans = 1;
  scanf("%d", &n);
  int i;
  for(i=1;i<=n;i++) ans *= i;
  printf("%d", ans);
}
```
