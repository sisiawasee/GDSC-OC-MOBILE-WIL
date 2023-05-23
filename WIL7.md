# WIL#7
> UI 구현해보기(3)
0. Flutter로 웹툰 앱 만들기 강좌 #4 POMODORO APP
  * User Interface
    - flexible Widgets: 서로 다른 크기의 화면에서 비율을 설정할 수 있도록 함, 하드코딩 대신 사이즈 조정 가능
    - onPressed: 버튼 클릭 시 실행되는 함수
    - Expanded Widgets: 화면 시작부터 끝까지 확장 -> row, column 등과 함께 사용해 가로/세로 방향 조절
    - 이외 alignment, color theme 설정(context), screen 폴더 생성 등 확인
  * Timer
    - conter에 입력할 totalSeconds 변수 초기화
    - onPressed 함수 설정: Timer->dart 표준 라이브러리를 통해 카운터 설정 (late modifier 예시)
    - timer=Timer.periodic(Duration(second:1), onTick): 1초마다 함수 실행
    - onTick method: 타이머가 바뀔 때마다 HomeScreenWidget setState 실행 ->totalSeconds--; (인자로 timer 받기)
  * Pause Play: boolean property inRunning을 받아 Icon과 실행 상태 조정
    - isRunning? Icons.():Icons.(): true/false 여부에 따라 아이콘 변경
    - onPressed에만 카운트를 시작해야 하므로 -> setState 설정 외에도 onPausePressed() method 구현
  * Data Format: Pomodoro를 완료한 숫자 추가
    - onTick이 0이 되면 다시 카운터를 중지하고 1500으로 초기화
    - 
1. DART 시작하기 #4 CLASSES ½ (~#4.5)
  * 생성자(constructor) 
    - 함수와 같이 named/positional로 구분됨
    - :this.(변수명)=(변수값)으로도 사용 가능
  * Cascade Notation: ..(변수명) 혹은 ..(함수명)으로 사용 가능
    - 앞의 '.'이 앞선 class를 지칭하는 this의 역할
* * *
[Q1.] setState가 UI에만 영향을 미치는 UI 업데이트 메소드가 아니라 실제로 다른 메소드 실행 여부에도 영향을 주는 건가요? isRunning이 setState에 의해서 true로 바뀌는 것이 살짝 헷갈립니다. 즉, 실제 변수값->UI 영향 뿐 아니라 UI->변수값으로도 영향을 주는 걸까요?

[Q2.] 
