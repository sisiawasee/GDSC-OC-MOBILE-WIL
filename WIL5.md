# WIL#5
> UI 구현해보기
0. Flutter로 웹툰 앱 만들기 강좌 #3  UI CHALLENGE
 * Header: Appbar 삭제, row, columm, scaffold 복습/각종 Widget 확인
   - align 메소드로 정렬하기, opacity로 투명도 조절하기 등
   - sized box와 child/children으로 간격 조정
 * Developer Tools:  devtool을 통해 row, columm 등 관계, 넓이 등 정확한 수치 계산
 * Buttons Section: BoxDecoration 메소드 사용
 * VSCode Settings&Code Action: 각종 VSCode 세팅과 코드 리팩토링, 단축키 안내
 * Reusable Widgets&Reusable Cards: 코드 재사용을 위한 위젯 추출(Extract Widget)
   - Widgets 파일 생성 및 컴포넌트 사용
   - class로 property 적용, text등을 상속 받은 위젯 작성 가능
   - SingleCHildScrollView 사용해 scroll 가능한 widget 사용, Offset을 음수 값을 주게 되면 overflow 가능
 * Cards&Icons and Transforms: overflow된 icon 넣기-clipBehavior: Clip.HardEdge
1. Dart 시작하기 #3강: FUNCTIONS
 * positional parameter와 named parameter 두 가지 방법으로 변수 선언
   - positional의 경우 기본적으로 required, named의 경우 required 선언 필요
   - positional을 not required로 선언해주고 싶다면 대괄호와 nullable 선언 (Ex: [String? country])
   - default와 nullable 명시 해주어야 함
   - QQ 연산자: 변수가 null이라면 우항 대입
   - typedef: class보다 간단한 경우의 type alias 설정

* * *
[Q1.] QQ연산자를 썼을 때 코드 단축과 가독성 외에도 이점이 있을까요?

[Q2.] #3.3강에서 VSCode Settings를 수정할 때 json 파일을 수정하게 되어있는데요, 언어가 달라도 한 파일로 묶일 수 있는지, json 문법도 알아야 하는지 궁금합니다.
