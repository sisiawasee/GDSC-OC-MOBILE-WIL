# WIL#8
> UI 구현해보기(4)
0. Flutter로 웹툰 앱 만들기 강좌 #4 WEBTOON APP
  * AppBar
    - flutter는 위젯 식별을 위해 ID 사용, screen마다 dart 파일 구분 사용
    - Appbar: foregroundColor/backgroundColor 구분(title style과 fore~은 별개), elevation으로 음영
  * Data Fetching
    - services 폴더->apiService dart 파일 생성
    - baseUrl class 생성 -> 인스턴스 변수로 today를 받아오고, json 데이터 불러오기
    - API 요청-> json을 콘솔에 불러오기: getTodayToons 메소드-> pub.dev http 라이브러리 설치 (pubspec.yaml에 붙여넣기)
    - get함수: http 패키지로부터 불러오기 ->namespace 사용하기(as 구문, http.get(url) 등)
    - future: 비동기 프로그래밍 ->API요청에 따라 완전히 수행할 때까지 기다리기(await ->async function 선언), 미래의 결과 값 타입을 알려줌 ->실행 완료 시 <(타입명)>을 받는다고 명시
  * fromJson: Json 형식의 데이터를 클래스로 바꿔주기
    - webtoon class의 proprerty: title, thumb, id-> constructor 선언
    - jsonDecode 함수 사용: string으로 입력, dynamic 타입으로 반환 -> 리스트로 나눠서 입력받기
  * waitForWebToons: 웹툰에 대한 내용을 console이 아닌 화면에 출력하기 (await, initState override 등)
  * FutureBuilder: statelessWidget을 이용하여 API data fetch하기
    - Future class 이용(지난 시간에 만들어 놓은 class): build 메소드에 future 전달 ->FutureBuilder widget 이용
    - FutureBuilder: builder 매개변수->UI를 그려줌, initial Data, Future 전달(await 불필요)
    - snapshot: Future의 상태 catch->변화 여부 return -> 비동기 위젯을 사용하여 stateless 위젯 유지
  * ListView: FutureBuilder에서 ListView 반환
    - ListView: 많은 양의 데이터와 항목을 나열하는 위젯, 자동으로 scrollview 생성
    - 최적화 ListView=Listview.builder: 스크롤 방향 등 선택의 폭이 넓어짐, 아이템 개수 설정 가능, build 함수로 아이템 인덱스에 접근
    - listView.sperated: 리스트+구분자 반환
  * Webtoon Card
    - extract method->builder의 반환 동작을 method로 분리하기
    - expanded: 화면의 남는 공간을 차지하는 widget ->무한한 높이 제한, child를 확장하여 남는 공간을 채움
    - image.network(이미지 링크), clipBehavior로 부모 영역 침범 제한
  * Detail Screen: GestureDetector->동작 감지
    - onTap: 버튼 클릭 감지->새 함수 등록
    - 새로운 스크린 페이지 등록(StatelessWidget) ->클릭 시 해당 웹툰 정보 노출: 위젯을 실제 화면처럼 구현
    - Navigator: push route-> StatelessWidget X MeterialPage Route-> 다른 스크린처럼 보여줌, builder를 통해 route 만들기 (builder:(context)=>함수())
  * Hero: HeroWidget->애니메이션을 통한 화면 전환, 원래 화면의 위젯을 노출시킴, tag 사용
  * ApiService: API 이전과 같은 내용 json으로 받아오기
  * Futures: 초기화 property, late 주의 ->다른 위젯으로부터 argument 받아오기
  * Detail Info: (UI 제작) FutureBuilder로 snapshot 받아서 sanpshot.hasData로-> 데이터 받아오기
  * Episodes: Overflow시 singleChildScrollView로 감싸기
  * Url Launcher: 브라우저에서 Url 열기->url_launcher 패키지 설치
    - 버튼에 GestureDetector 추가 후 async await 사용해 올바른 URL 열기(launchUrlString 또는 launchUrl 등 사용)
  * Favorites: 휴대폰 저장소에 데이터 담기 ->shared_preferences 패키지 설치
    - 휴대폰 저장소와 connection 생성, getInstance->자료형 등 설정 가능
    - ID를 리스트로 저장해 리스트에 있으면 버튼에 반영: 새로운 클래스 지정 후 초기화 시 getInstance()하기
1. DART 시작하기 #4 CLASSES complete (#4.6~)
  * Enum: 타입에 포함되는 일종의 변수 생성(ex: Enum team(){blue, red})
  * abstract class: 추상화 클래스 ->상속받는 클래스가 어떤 메소드를 갖고 있어야 하는지 강제함
  * Inheritance: 상속
    - extends로 상속 가능 상속받는 함수의 생성자 함수 호출 필요
    - 변수를 받아주고 : super(변수이름)을 통해 부모 클래스의 생성자 갖고오기
    - 메소드 override(대체) 가능-> @override, 코드 재사용 또한 가능 (super 이용)
  * Mixins: 생성자가 없는 클래스->클래스에 프로퍼티 추가 시 사용
    - with으로 사용, 상속 X(부모 클래스 X), but 여러 클래스에 재사용이 가능함
2. 7주차 과제 TODO
  * API 사용해 아무 기능이나 추가해 보기 -> 클릭 시 보더콜리 사진 랜덤 출력
* * *
[Q1.] future은 타입명이 아니라 final 같은 타입 수식어의 개념이라고 생각하면 될까요?

[Q2.] GestureDetector 위젯에서  Navigator.push 메소드를 사용할 때 새로 로딩된 카드 화면을 끄거나(X) 이전 화면으로 돌아갈 때(<) 나오는 아이콘을 바꿀 수도 있을까요?

[Q3.] GestureDetector 위젯을 이용하여 보더콜리 사진 노출 시 좋아요 기능을 추가해 좋아요를 누르면 하트 아이콘만 뜨고, 좋아요를 누르지 않았을 때는 사진이 뜨게 하고 싶은데, isLiked bool 변수를 추가해서 onTap과 setState 메소드를 사용하면 오류가 뜹니다. image에는 child가 없어서 index로 구분을 해야할 것 같은데, random이라 API json에도 딱히 ID나 식별자가 없는 것 같아 고민입니다. 어떻게 해야 할까요?
