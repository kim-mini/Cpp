# Cpp 


## day 1

네임스페이스

: 김철수의 '김'과 같은 성을 의미

```cpp
std::cout
```

std가 김이고 cout가 철수라고 보면 된다

위에서 ``using namespace std``를 적어주면 
std::를 생략하고 cout만 적을 수 있다

```cpp
// 콘솔화면에 출력하는 프로그램 작성 
#include <iostream>

// 프로그램이 시작될 때 가장 먼저 시작되는 지점
int main() {
  std::cout << "Hello World!\n"<<std::endl;
  return 0;
}
```

```cpp
// 콘솔화면에 출력하는 프로그램 작성 
#include <iostream>

// 해당 네임스페이스를 사용
using namespace std;

// 프로그램이 시작될 때 가장 먼저 시작되는 지점
int main() {
  cout << "Hello World!\n"<<endl;
  return 0;
}
```

여기에서 cout는 iosteam에 정의 되어있다

: 콘솔 아웃이라는 뜻, 콘솔창에 출력해준다

## day 2
