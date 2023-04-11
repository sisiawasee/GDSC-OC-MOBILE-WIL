# WIL#3
> 가로세로 배치와 Scaffold
0. 코딩애플 쉬운 플러터 2강 : 가로세로 배치하는 법과 Scaffold
 * MaterialApp, 쿠퍼티노를 통해 Google/iOS에서 위젯, UI를 가져올 수 있음.
   - 커스텀 디자인을 하더라도 MaterialApp 포함→많은 코드와 메모리를 절약 가능함.
 * Scaffold : 어플리케이션을 상/중/하 레이아웃으로 나눠줌.
   - appBar, body(내용 영역), bottomNavigationBar
 * Row/Column : 가로/세로로 여러가지 위젯 추가 (children[] 사용)
   - 정렬 : (가로축 정렬) MainAxisAlignment.(정렬위치) (ex. SpaceEvenly →CSS의 display:flex와 유사), (세로축 정렬) CrossAxisAlignment.(정렬위치)
   - Container를 사용해서 Row/Column의 위젯 사이즈를 정해줄 수도 있음.
 * ctrl+space바로 자동완성 가능, (타입).(함수명)→함수실행
1. Dart 시작하기 #2강 : Data types
 * Dart의 데이터 타입 : 기본(var, int, float, double...), lists, maps, sets
   - 기본 : 컴파일러에서 지정할 수 있도록 var를 기본으로 쓰되 class에서는 명시해줄 것, dart는 객체지향언어이기 때문에 모든 변수 타입이 객체가 됨, 특히 float/double/int 같은 숫자는 num class 를 상속받음
   - lists : list에 변수 추가 시 조건을 따지는 collection if와 타 list로부터 불러오되 추가적인 행위를 해줄 수 있는(String Interpolation 등) collection for 존재
   - Maps : python의 dictionary와 같은 개념. 키-인덱스로 구성되어 있음.
   - Sets : python의 set과 동일. 모든 요소가 유일함.

* * *

[Q1.] children[]라고 표기할 때, 그럼 children은 list속성을 일부 상속받는 게 맞나요?

[Q2.] 2개 이상의 위젯을 넣을 때는 children, 하나는 child로 이해했는데 1개의 위젯을 넣을 때도 children을 써야한다던가 하는 예외의 경우도 있을까요?
