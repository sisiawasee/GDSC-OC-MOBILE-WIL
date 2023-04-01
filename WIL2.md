# WIL#2
> 간단한 flutter 앱 구현과 기본 문법
0. 코딩애플 쉬운 플러터 1강 : 기본 위젯 4개만 알면 기초 끝
 * void main과 stless로 기본 앱 세팅
   - flutter 프로젝트 생성 후 린트를 끄고 lib 폴더의 main.dart에서 코딩 시작
   - main 함수를 제외한 google의 기본 제공 세팅을 삭제하고 stless 입력으로 앱 메인 화면 구현 (기능 부여)
 * flutter 앱 디자인 : 위젯 짜깁기
   - 글자 위젯 : Text('contents')
   - 아이콘 위젯 : Icon(Icons.아이콘 이름)
   - 이미지 위젯 : Image.asset('이미지 경로') →assets 등 이미지 보관용 폴더를 만들고, 디렉토리 설정 (pubspec.yaml 파일에서 flutter 코드 아래에 assets: - assets/ 설정)
   - 박스 위젯 : Container() or SizedBox() →폭(width), 높이(height), 색(color) 설정 (스타일 명 : 값), 단위는 LP
   - 센터 위젯 : Center() →자식 요소를 중앙정렬하는 위젯

1. Dart 시작하기 #1강 : Variable
 * Dart의 변수 선언 : var, dynamic과 수식어 late, final, const
   - var : 파이썬처럼 자동으로 변수의 타입을 지정해 줌.
   - dynamic : 변수 타입을 여러 번 바꿀 수 있음.
   - final : javascript에서의 const와 유사함. 한 번 지정한 값을 변화시킬 수 없음.
   - const : 이미 알고 있는 상수값 지정 시 이용.
   - late : 사용자나 API로부터 값을 받아올 때 변수 값을 지정하지 않고도 변수 선언을 가능하게 함. final이나 var 앞에 주로 사용.

* * *

[Q1.] flutter의 위젯으로 반응형 디자인이 가능하면 제트플립에서의 반응형 디자인도 설계가 가능할까요?

[Q2.] main 함수에서 runApp 구동 시 시작되는 것이 메인 화면이라고 이해했는데, 스플래시 화면 같은 앱 시작 화면은 어떻게 세팅할 수 있나요? main 전에 선언을 해줘야 하나요?
