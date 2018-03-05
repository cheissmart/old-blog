<center><h1>Can I Pass -- Advance</h1></center>

#### Discription:
```markdown
input a score. if the score is not in the range (0 <= score <= 100), input again until the score is valid;
output "Pass" if the score >= 60 and "Fail" if the score < 60
```

### canIpassAdv.cpp
```markdown
#include <iostream>

using namespace std;

int main()
{
  int score;
  while(cin >> score && (score < 0 || score > 100));
  if(score >= 60) {
    cout << "Pass" << endl;
  }
  else {
    cout << "Fail" << endl;
  }
}
```

### canIpassAdv.c
```markdown
#include <stdio.h>

int main()
{
  int score;
  while(scanf("%d", &score) != EOF && (score < 0 || score > 100));
  if(score >= 60) {
    printf("Pass\n");
  }
  else {
    printf("Fail\n");
  }
}
```
