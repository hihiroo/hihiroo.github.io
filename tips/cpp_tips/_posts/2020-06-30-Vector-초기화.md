2020.06.29   
___

# Vector 초기화

std::vector를 초기화하는 방법에는 대표적으로 2가지가 있습니다.

```c++
#include <vector>
#include <iostream>
using namespace std;
int main(){
    vector<int> a(10,-100);
    vector<int> b = {1,2,3,4,5};
}
```

첫번째 vector<int> a(10,-100);은 a벡터에 -100이 10개 들어가게 되고, 선언과 동시에 모든 값을 같은 값으로 초기화 시킬 때 사용됩니다.

fill이나 memset 함수를 사용하지 않아도 되기 때문에 매우 간편합니다.

두번째 vector<int> b = {1,2,3,4,5};은 C++11부터 사용가능한 문법인데, 배열을 초기화 시키는 것과 사용법이 유사합니다.

벡터 값을 하나하나 지정해서 초기화 시킬 수 있다는 매우 강력한 장점을 가지고 있습니다.