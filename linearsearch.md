<center><h1>Linear Search</h1></center>

#### Discription:
```cpp
Time complxity: O(n)
```

### Linear_Search.cpp
```cpp
#include <iostream>

using namespace std;

int linear_search(int *a, int n, int val) {
    for(int i=0;i<n;i++)
        if(a[i] == val)
            return i;
    return -1;
}

int main()
{
    int a[100], n, qry;
    cin >> n;
    for(int i=0;i<n;i++)
        cin >> a[i];
    cin >> qry;
    int result = linear_search(a, n, qry);
    if(result != -1) {
        cout << "Query found at " << result << endl;
    } else {
        cout << "Query not exists" << endl;
    }
}
```

