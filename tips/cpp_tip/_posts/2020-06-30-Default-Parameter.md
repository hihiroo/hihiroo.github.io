----
layout: post
title: Default Parameter
noindex: true
---

<https://boycoding.tistory.com/222>

```c++
#include <iostream>
using namespace std;
void f(int x, int y = 10, int z = 3){
    cout << x << " " << y << " " << z << '\n'; 
}
int main(){
    f(1); //1 10 3
    f(1, 5); // 1 5 3
}
```

f함수의 매개변수 중 int y = 10과 int z = 3은 디폴트 매개변수입니다.

f함수를 호출할 때, y값에 대한 정보를 제공하지 않으면 디폴트 값인 10을 갖게 됩니다.

따라서 어떤 기본 값을 가지고 있지만 필요에 따라 값을 변경하고 싶을 때 디폴트 매개변수를 이용하면 편리합니다.

디폴트 매개변수는 여러개 쓸 수 있고, 가장 마지막 변수자리부터 연속으로 채우면 됩니다.

유의하여야 할 점은, 함수를 호출할 때 전달인자(Argument)가 가장 왼쪽 매개변수부터 채워지기 때문에 y는 디폴트 값을 쓰고 z는 값을 변경하는 것은 안됩니다.