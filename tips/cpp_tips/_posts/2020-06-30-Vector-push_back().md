
---
layout: post
title: Vector push_back()
noindex: true
---



<https://www.youtube.com/watch?v=SaZ3jf6gxn4>

std::vector의 끝에 데이터를 추가하는 push_back은 일반적인 경우 O(1)의 Time complexity를 따릅니다.  

하지만 벡터가 있는 메모리에 더 이상 연속된 빈 공간이 없을 때, 즉 벡터의 capacity를 초과하면 더 큰 메모리 공간을 찾아 벡터를 복사해 옮기는 과정을 거치기 때문에 O(n)이 됩니다.  

따라서 벡터에 추가할 데이터의 개수가 많을 때 push_back은 완벽히 O(1)이 아니기 때문에 시간초과를 유의하셔야 합니다!  

<br>

```c++
#include <iostream>
#include <vector>
using namespace std;
int main(){
 vector<int> v;
 v.reserve(1000000);
 cout << v.size(); // 0
 cout << v.capacity(); // 1000000
}
```

push_back을 꼭 써야한다면 최대 데이터 크기만큼 벡터의 capacity를 정해놓는 방법으로 시간을 절약할 수 있습니다.