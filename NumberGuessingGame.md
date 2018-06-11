<center><h1>Number Guessing Game</h1></center>

#### Discription:
```cpp
# sample 
out:  0 < ? < 100
in:   50
out:  wrong answer, guess smaller
out:  0 < ? < 50
in:   30
out:  wrong answer, guess larger
out:  30 < ? < 50
int:  45
out:  bingo answer is 45
```

### NumberGuessingGame.cpp
```cpp
#include <bits/stdc++.h>

using namespace std;

int main()
{
  srand(time(NULL)); // use current time as seed for random generator
  int ans = (rand() % 99) + 1, l = 0, r = 100;
  while(true) {
  	cout << l << " < ? < " << r << endl;
    int guess;
    cin >> guess;
    if(guess == ans) {
    	cout << "bingo answer is " << ans << endl;
    	break;
	}
	else if(guess < ans) {
    	cout << "wrong answer, guess larger" << endl;
    	l = guess;
	} else {
		cout << "wrong answer, guess smaller" << endl;
    	r = guess;
	}
  }
}
```

### NumberGuessingGame.c
```c
NA
```
