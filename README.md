#  int main  vs  void main  vs  main
한 줄 요약 : 아무차이없다. 

but 내부적으로 차이가 있다

int main()은 main() 함수가 종료할때 정수형 값을 리턴,
void main() 하면 main() 함수가 종료할때 아무 값도 리턴하지 않으며,
main() 하면 void main() 과 같다.

운영체제는 프로그램이 종료할때 main() 함수의 리턴값을 받아보고 프로그램이 왜 종료되었는가를 판단합니다.
main() 함수가 0 을 리턴하면 프로그램이 정상적으로 실행을 마치고 종료한것으로 간주하고, 
0 이외의 값을 리턴할 경우 비정상적으로 종료된것으로 간주한다.

참고로, C언어 표준이 제시하는 가장 이상적인 main() 함수의 정의문은 이렇다.
-> int main( int argc, char *argv[], char *env[] )

# return 0; 를 쓰는 이유
return 0; -> int 0을 반환한다는 뜻이다.

원래는 C언어에서 main의 경우 return 0;를 써서 에러 없이 끝났다는 것을 운영체제에게 알려주었다.
그러나 시간이 지나면서 C++ 표준에서 main이 값을 리턴하지 않아도 main이 끝나면 암묵적으로 0을 return 하는 것으로 인정했고, 
따라서 main에서 만큼은 값을 return하지 않아도 정상적으로 실행된다.
