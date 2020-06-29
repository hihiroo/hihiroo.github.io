
2020.06.29   
___

# Map count

<http://www.cplusplus.com/reference/map/map/find/>
<http://www.cplusplus.com/reference/map/map/count/>

<br>

std::map에서 특정 key값의 유무를 확인 할 때 count 함수를 쓰면 코드를 더 짧고 직관적이게 짤 수 있습니다!

map에서 key값을 찾을 때 정석적인 방법은 find 함수를 이용하는 것입니다.

```c++
map1.find(key) != map1.end() 
```

그러나 변수명이 길다면 코드가 길어져 가독성이 떨어지기 때문에 코드 길이도 비교적 짧고 직관적으로 의미를 알 수 있는 count 함수를 쓰는 것을 추천드립니다.

```c++
map1.count(key) > 0
```

<br>

` 두 방법 모두 O(logn)이지만 평균적으로 find가 count보다 약간 더 빠릅니다. `

<https://stackoverflow.com/questions/25490357/checking-for-existence-in-stdmap-count-vs-find>