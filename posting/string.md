
2020.06.29   
___

# String


<http://www.cplusplus.com/reference/string/string/operator+=/>
<http://www.cplusplus.com/reference/string/string/operator+/>

std::string에서 문자열 2개를 합칠 때 쓰는 operator += 과 operator +는 완전히 다릅니다!

operator += 는 기존의 문자열 끝에 새로운 문자열을 붙이는 것이고, operator +는 두 개의 문자열을 합친 새로운 문자열을 만드는 것입니다.

따라서 operator += 는 뒤에 추가되는 문자열의 길이만큼의 시간이 걸리는 반면, operator +는 **합쳐진 전체 문자열의 길이 만큼의 시간**이 걸립니다.

만약 a라는 문자열 뒤에 b라는 문자열을 붙일 때, a의 길이가 100만이고 b의 길이가 1이라면 a = a + b가 **a += b보다 100만배 느린 연산**을 하게 되는 것입니다.  

문자열의 길이가 길다면 **operator +는 지양**하는 것이 좋습니다!