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
  * 
* * *
[Q1.] future은 타입명이 아니라 final 같은 타입 수식어의 개념이라고 생각하면 될까요?

[Q2.] 
