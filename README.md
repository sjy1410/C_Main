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
