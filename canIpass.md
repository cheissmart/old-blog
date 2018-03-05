<center><h1>Can I Pass ?</h1></center>

### canIpass.cpp
```markdown
#include <iostream>

using namespace std;

int main()
{
  int score;
  cin >> score;
  if(score >= 60) {
    cout << "Pass" << endl;
  }
  else {
    cout << "Fail" << endl;
  }
}
```

### canIpass.c
```markdown
#include <stdc++.h>

int main()
{
  int score;
  scanf("%d", &score);
  if(score >= 60) {
    printf("Pass\n");
  }
  else {
    printf("Fail\n");
  }
}
```
