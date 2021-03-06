# Node-JS
  
  PC나 스마트폰에서 사용하는 프로그램 >> 애플리케이션(앱)
  프로그램을 직접 만들어 보려면 직접 API를 알아야 한다
  
  + API-프로그램을 쉽게 제작할 수 있게 미리 만들어 놓은 것들의 모음
  + 클라이언트 - 다른 곳에 있는 단말에 데이터를 달라고 요청하는 프로그램
  + 서버 - 다른 곳에서 요청받은 명령을 처리해주는 프로그램
  인터넷에 연결하기 위해서는 단말에 네트워크 카드(또는 인터넷 카드)가 들어있어야 한다
  + 웹서버 - 웹 브라우저에 접속하는 서버, HTTP 프로토콜 사용
  
  + 에이잭스(Ajax) - 비동기식 자바스크립트 XML의 약자
    웹서버에서 웹 문서를 받아오는 것이 아니라 데이터를 받아오기 위한 방법과 기술
    
  + 사물인터넷 - 다양한 센서로부터 값을 전달 받아 동작
  
  웹서버는 웹 프레임워크인 익스프레스로 기본 구조를 만든다
  
  뷰템플릿은 클라이언트에 응답을 보낼 때 웹 문서의 원형을 만들어 놓은 것
  
  localhost - PC자신을 나타내는 인터넷 주소, 위치정보 = 공간 데이터
  
  몽고디비 - 비정형화 / MYSQL - 정형화
  
  
  
  + 자바스크립트를 이용해 서버를 만들 수 있는 개발 도구
  웹서버에 파일 업로드 할 때 업로드 완료되기 전까지 웹 서버의 데이터 조회 등 다른 작업 불가
  이를 해결하기 위해 만들어진 새로운 방식의 서버 개발 도구
  
  EX) 웹브라우저로 PC에 있는 문서 파일 하나 업로드
  파일의 크기가 크면 파일 업로드에 많은 시간 필요
  
  파일 업로드 완료전까지 서버에 있는 다른 파일의 정보 확인이나 파일 업로드 상태 요청 불가
  
  ▶이러한 문제 해결을 위해 만든 것이 노드(하나의 요청처리 끝남을 기다리지 않고 다른 요청 동시 처리 가능)
  
  ▶비동기 입출력(논블로킹 입출력)
  
  
    동기 입출력 방식으로 파일을 읽는 경우 파일 기능 읽기 요청후 대기하지만
    비동기 입출력 방식에서는 대기하지 않고 다른 작업 진행, 데이터 처리 시점에서 콜백 함수 호출
    
    자바스크립트에서는 on() 메소드를 사용해 이벤트를 콜백함수와 바인딩(binding) 할 수 있다
    ▶응답 객체 res 객체의 on()메소드를 사용해 data 이벤트와 콜백 함수 바인딩
      ▶data라는 이름의 이벤트 받을 시 등록한 콜백 함수 

+ 바인딩(Binding)은 "서로 묶어서 연결해준다"의 의미

  ▶버튼이 하나 있고 이 버튼 클릭시 click 이벤트 발생 ▶ click 이벤트 함수와 바인딩
    
    ▶click 이벤트 발생시 해당 함수 수행
    
  [객체].on([이벤트 이름],[함수 객체]); ▶ res.on('data', function() {...});
  
  
  크롬 브라우저는 최신의 웹표준을 가장 준수하며 사용하는 사람들이 많은 사람들이 사용하는 브라우저
  
  + JSON 포맷
    자바스크립트의 객체 포맥
    
    단말끼리 데이터 주고 받을때 주로 사용
    
    { } 를 사용해 객체 생성 (그 안의 키와 값으로 구성된 속성을 가지고 ,로 구별)
    
Consolo 객체의 주요 메소드

  메소드             설명

dir(object) ------- JS 객체의 속성들 출력

  time(id)  ------- 실행 시간 측정 위한 시작 시간 기록
  
timeEnd(id) ------- 실행 시간 측정 위한 끝시간 기록


+ 함수와 메소드 차이

  함수 - 어떤 기능을 정의하고 이런 기능을 가진 하나의 단위
  
  메소드 - 객체 지향 언어에서 함수를 부르는 말?
  
  ▶ 이름을 어떻게 부르든 의미 전달에 큰 
  
전역변수 (Global Variable) - 코드에 어느부분에서든 사용할수 있는 변수

process 객체 - 프로그램 실행시 만들어지는 프로세스 정보를 다루는 객체

argv - 프로세스를 실행할 때 전달되는 파라미터(매개변수) 정보
env - 환경 변수 정보
exit - 프로세스를 끝내는 메소드
외장 모듈 - 다른 사람이 만들어둔 모듈

npm의 역할 - Nodepakage Manager의 약자
            노드의 패키지를 사용할 수 있도록 설치 및 삭제등을 
            
모듈 - 외부의 영향을 받지 않는 독립된, 재사용 가능한 코드들의 묶음,
       모듈로 API를 묶어줌에 변수나 함수들의 name space를 보장해주고 모듈화를 통한 기능적 코딩이 가능해짐
       
require() - 외부 모듈을 가져올수 있는 메소드, 파라미터로 추가할 모듈의 파일 경로값을 받음

module.exports - node가 만들어낸 property인데 빈 object가 대입되어 있다
                 메서드를 대입하게 되면 function object가 빈 object를 덮어쓰게 된다
              
module과 require 생성

require 메서드가 작동하는 원리 이해전 먼저 require와 module이 어떻게 생성되는지 살펴보면
터미널 커맨드에 node를 실행시키고 this를 입력해보면 NodeJS가 local object에 module property를 생성하여 Module object를 대입하고
require method를 추가하였음이 확인 가능하다

NodeJS는 각각의 모듈마다 module property와 require mothod를 만들어 준다. 모듈끼리 소통하기 위해서 이들을 활용하게 된다
이 medule과 require는 global object에 붙은 하나의 static property가 아니다. 이들은 local object로서 각 모듈마다 하나씩 가진
API이다.

여러 모듈을 한번에 가져오는 방법

1)index.js  - require 메서드가 특별히 인식하는 파일로서 여러 모듈을 가져온다
2)폴더에 모듈 추가 - greet폴더 안에 모듈 파일들을 추가해줍니다. module.exports = (~)
3)index.js에서 require 하기
4)app.js에서 requir 하기
