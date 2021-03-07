# Cpp 


## day 1

``네임스페이스`` : 김철수의 '김'과 같은 성을 의미

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

``cout`` : 콘솔 아웃이라는 뜻, 콘솔창에 출력해준다

## day 2

``cout과 cin``

iostream 에 정의 되어있다.

``cout`` : 콘솔아웃이란 뜻, 콘솔 창에 출력

``cin`` : 콘솔인 이라는 뜻 콘솔 창에서 값을 입력 받음
 
```cpp
// 콘솔화면에 출력하는 프로그램 작성 
#include <iostream>

// 해당 네임스페이스를 사용
using namespace std;

// 프로그램이 시작될 때 가장 먼저 시작되는 지점
int main() {
  int input = 0;
  cin >> input;
  cout << input << endl; 
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
  // 문자열 콘솔 출력
  char input[7];
  cin >> input;
  cout << input << endl;
  return 0;
}
```
---

### if

```cpp
// 해당 숫자가 짝수이면 짝수라고 알려주는 프로그램을 작성해보자
#include <iostream>

using namespace std;

int main() {
  int input;
  cin >> input;
  if (input%2 ==0){
    cout << "짝수입니다" << endl;
  }
  else{
    cout << "홀수입니다" << endl;
  }
  return 0;
}
```

### else if

```cpp
// 해당 숫자가 짝수이면 짝수라고 알려주는 프로그램을 작성해보자
#include <iostream>

using namespace std;

int main() {
  int number;
  cin >> number;
  
  if (number < 10){
    cout << "10보다 작은 수 입니다" << endl;
  }
  else if (number < 20){
    cout << "20보다 작은 수 입니다" << endl;
  }
  return 0;
}
```


```cpp
// 세 개의 float 형 숫자를 사용자에게 입력 받아서 가장 큰 수를 출력하는 프로그램을 작성하라.

#include <iostream>

using namespace std;

int main(){
  float f1, f2, f3 = 0.0;
  float fmax = 0.0;
  cout << "f1 입력해주세요" << endl;
  cin >> f1;
  cout << "f2 입력해주세요" << endl;
  cin >> f2;
  cout << "f3 입력해주세요" << endl;
  cin >> f3;
  
  if (f1 > f2){
    fmax = f1;
  }
  else{
    fmax = f2;
  }
  
  if (fmax < f3){
    fmax = f3;
  }
  cout << fmax << endl;
  return 0;
}
```


### switch

```cpp
// 해당 숫자가 짝수이면 짝수라고 알려주는 프로그램을 작성해보자
#include <iostream>

using namespace std;

int main() {
  int number = 0;
  cin >> number;
  
  switch(number){
    case 1:
      cout << "1입니다" << endl;
      break;
    case 2:
      cout << "2입니다" << endl;
      break;
    case 3:
      cout << "3입니다" << endl;
      break;
  }
  return 0;
}
```
