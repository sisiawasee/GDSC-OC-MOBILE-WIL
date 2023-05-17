# WIL#6
> UI 구현해보기(2)
0. Flutter로 웹툰 앱 만들기 강좌 #4 STATEFUL WIDGETS
 * State: State 여부에 따른 위젯 분류
   - StatelessWidgets: build method를 통해 UI를 출력하기만 함
   - StatefulWidgets: data가 반응형으로 변형됨, 상태를 가지는 위젯 ->not final
 * setState&Recap: State class에 data가 변경됨을 알림
 * BuildContext
   - theme과 Themedata 선언, family style
   - 위젯 트리에서 위젯의 위치 제공, 상위 요소 데이터 접근 가능
 * Widget Lifecycle
   - initState(): 상태 초기화 ->필수 X, 항상 build 메소드보다 앞에 호출되어야 함
   - dispose(): 위젯이 스크린에서 제거될 때 사용 (SatefulWidget 자체는 존재)

* * *
[Q1.] 앞선 강의의 오른쪽 상단 모서리를 잘라내는 카드 섹션을 어떻게 만들 수 있을까요? 커스터마이징하는 방법이 궁금합니다.

[Q2.] statefulWidget을 쓰지 않아도 data가 변경되는 것이 반영될 수 있을까요? 위젯에는 보여지지 않아도(=UI 구현은 안하더라도) 변수 변형은 가능한지 궁금합니다.
