<center><h1>Can I Pass ?</h1></center>

#### Discription:
```markdown
input a score (0 <= score <= 100)
output "Pass" if the score >= 60 and "Fail" if the score < 60
```

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
#include <stdio.h>

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
