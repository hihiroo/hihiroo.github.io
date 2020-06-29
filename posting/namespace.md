2020.06.29   
___

# namespace

<http://www.cplusplus.com/doc/oldtutorial/namespaces/>
<https://en.cppreference.com/w/cpp/header/iostream>

```c++
#include <iostream>
using namespace std;
int main(){
 cout << "hello";
}
```

c++ 에서 using namespace std; 는 왜 쓰는 걸까요?

위의 코드에서 using namespace std;  부분만 지우면, cout이 선언되어 있지 않다는 에러가 뜨는 것을 확인할 수 있습니다.

컴파일러가 cout이 어디에서 정의된 함수인지 알 수 없다는 것인데요,  std::cout << "hello";  로 바꿔주면 정상적으로 컴파일이 됩니다.

iostream 라이브러리를 보면 cout은 std라는 namespace 안에 있는 것을 확인 할 수 있는데, namespace는 "이름 공간" 이라는 뜻처럼 변수나 함수에 대한 정의가 모아져 있는 공간입니다.

같은 이름의 식별자라도 namespace에 따라 구분할 수 있기 때문에 충돌 방지를 위해 사용합니다.

std::은 cout이 std라는 namespace 안에 있다고 알려주는 역할을 하는 것입니다.

```c++
#include <stdio.h>
namespace A{
  int x = 10;
}
namespace B{
  int x = 5;
}
int main(){
  printf("%d %d", A::x, B::x); // 10 5
}
```
using namespace std;는 식별자 앞에 std::를 붙이지 않아도 std namespace에서 찾게끔 하는 기능을 합니다.

따라서 std::cout 대신 cout을 써도 에러가 발생하지 않게 됩니다.

그렇다면 전역에서 선언된 식별자는 어떻게 구분을 할까요?

식별자 앞에 :: 을 붙이면 전역 영역에서 선언된 변수를 가져올 수 있습니다.

```c++
#include<iostream>
using namespace std;
int a = 10;
int main(){
  int a = 5;
  cout << ::a; // 10
}
```