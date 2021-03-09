# Cpp 
[cpp 공부 사이트](https://karupro.tistory.com)

## c++ basic
```cpp
#include <iostream>
using namespace std;

int main()
{
    return 0;
}
```

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

## day 3

```cpp
// HELLO, WORLD! 를 출력해 보세요.
// 자신의 이름을 출력해 보세요.
// 2020 을 출력해 보세요.
// 다음처럼 출력해 보세요:


#include <iostream>
using namespace std;

int main()
{
  cout << "HELLO, WORLD\n";
  cout << "김민이\n";
  cout << "2020\n";
  cout << "즐거운 C++ 프로그래밍 \n오늘은 출력을 연습하고 있습니다.";
  return 0;
}
```

```cpp
// sum이라는 정수형 변수를 선언해 보세요.
// 1부터 5를 곱한 값을 sum에 대입하고, 출력해 보세요.
// sum에 '5 팩토리얼'이라는 주석을 달아보세요.
// sum을 내포블록에 선언하고, 내포블록에서 출력해 보세요.


#include <iostream>
using namespace std;

int main()
{
    {
        int sum = 0; // 5 팩토리얼
        sum =  1 + 2 + 3 + 4 + 5;
        cout << sum;
    }
  return 0;
}
```
---

``int age = 0;`` <<  C언어식 초기화 방법 

``int age{0};`` << c++에서는 이렇게

``cpp``에서는 가급적 ``중괄호``를 활용해 ``변수 초기화``를 시켜주도록 하자

---

| 논리형 | bool | 1바이트 | true, false |
|------|------|--------|-------------|
|자동   | auto |        | 초기화한 자료형의 값 |

``boolean`` : bool 타입의 변수에는 숫자를 넣으면 안 되고 반드시 ``true``와 ``false``

```cpp
bool result{True};
```

``auto`` : 초기값의 자료형에 맞춰 ``변수의 형식을 자동``으로 결정해주는 역할

```cpp
// 그 대신 선언할 때 초기화를 동시에 해 줘야 합니다.
auto a = 123 // int
```

```cpp
#include <iostream>
using namespace std;

int main()
{
    auto str = "안녕하세요";
    cout << str << endl;
    return 0;
}
```

### decltype

- auto가 초기값에 맞추어 자동으로 형식을 결정했다면 decltype은 '~와 같은 자료형' 을 정해주는 것에 가깝습니다

- decltype(x) 라고 하면 x와 같은 자료형이 됩니다. 이때 x는 10, 3.14, 'A'와 같은 상수가 되어도 좋고, 이미 선언된 변수가 되어도 좋습니다

---

### 여러가지 자료형을 써보자

```cpp
#include <iostream>
using namespace std;

int main()
{
    int age{20};
    double pi{3.14};
    bool result{false};
    auto str{R"(평화롭고 따스한 "봄날"ㅎ)"};
    char ar{'\a'};
    
    cout << "나의 나이는 " << age << endl;
    cout << "원주율의 값은? "<< pi << endl;
    cout << "c++은 쉬워요? " << result << endl;
    cout << str << endl;
    cout << "알람아 울려라! " << ar << endl;
    return 0;
}
```

### 출력문을 한문장으로 묶을 수 있다

```cpp
cout << "나의 나이는 " << age << "살\n" 
    << "원주율의 값은? "<< pi << endl
    << "c++은 쉬워요? " << result << endl
    << str << endl
    << "알람아 울려라! " << ar << endl;
```

### printf() 연습해보기

```cpp
#include <iostream>
using namespace std;

int main()
{
    int age{20};
    double pi{3.14};
    bool result{false};
    auto str{R"(평화롭고 따스한 "봄날"ㅎ)"};
    char ar{'\a'};
    
    //cout << "나의 나이는 " << age << "살\n" 
    printf("나의 나이는 %d살\n", age);
    // << "원주율의 값은? "<< pi << endl
    printf("원주율의 값은? %.2f\n", pi);
    // << "c++은 쉬워요? " << result << endl
    printf("c++은 쉬워요? %d\n", result);
    // << str << endl
    printf("%s\n", str);
    // << "알람아 울려라! " << ar << endl;
    printf("알람아 울려라! %c\n", ar);
    return 0;
}
```

---

```cpp
// char 변수에 작은 따옴표를 저장하고, 출력해보세요.
// 날 문자열 리터럴을 사용해서 엔터를 출력해 보세요.
// std::printf() 함수를 통해 '50%'를 %d를 이용하여 출력해 보세요.
#include <iostream>
using namespace std;

int main()
{
    char str{'\''};
    // 날 문자열 리터럴 기본형은
    // ---> R"()"
    auto str2{R"(엔터를 
    출력하자)"};
    
    cout << str << endl;
    cout << str2 << endl;
    printf("%d%%",50);
    return 0;
}
```
