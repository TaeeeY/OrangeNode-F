# (주)롯데정보통신 사내 커뮤니티 사이트 프로젝트

### 프로젝트 개요
--------------------------------------
1. 프로젝트 주제 : 사내 커뮤니티, OrangeNode
2. 프로젝트 기간 : 2024-05-20 ~ 2024-06-21
3. 배경 및 목적 : 사내 커뮤니티를 개설해 보았습니다. 일정을 관리하고, project를 생성하고, 실시간 채팅을 통해 업무 효율화를 목적으로 합니다.
4. 담당한 기능: 채팅,게시판
5. 팀 구성 : 최이진, 김선광, 정원구, 김형민, 정태영


### 사용한 기술
--------------------------------------
Spring Boot, Java, REACT, HTML5/CSS3/JavaScript, MyBaits, JPA, AWS


### ERD
--------------------------------------
<details>
  <summary>ERD</summary>
  <br>
  <img src="https://github.com/Taeyoung20230727/OrangeNode-F/assets/140632598/fa7b5e68-a6dd-49f5-9e56-3fefc0154327" alt="ERD">
</details>



# 직접 구현한 기능 영상
--------------------------------------

## 게시판
<a href="https://youtu.be/awCfZnPH_Sc">
  <img src="http://img.youtube.com/vi/awCfZnPH_Sc/maxresdefault.jpg" alt="게시판 동영상" width="500"/>
</a>

## 채팅
<a href="https://youtu.be/GgoQ1-DBkQY">
  <img src="https://img.youtube.com/vi/GgoQ1-DBkQY/maxresdefault.jpg" alt="채팅 동영상" width="500"/>
</a>


### 이 프로젝트를 통해 배운 내용
--------------------------------------
✏️ React의 여러 hook (useState, useEffect, useRef 등) 들을 직접 사용해보며 사용 목적과 사용 방법을 알게 되었습니다.
<details>
  <summary>학습한 react hook 내용 </summary>
  <br>

  1. useState : 컴포넌트의 상태값을 선언하고 관리하는 hook입니다. const [count, setCount] = useState(0); 식으로 초기 값을 0으로 선언할 수도 있고, const [list, setList] = useState([])로 빈   배열 형태로 선언할 수도 있습니다. 혹은 const [user, setUser ] = useState({uid:'', name:"", age:0}) 이렇게 원하는 빈 객체 값으로 선언할 수도 있습니다.

  2. useEffect : 의존성 배열을 이용해, 상태값이 업데이트 될 때마다 실행할 수 있습니다.
  useEffect(() => { console.log("state name update..."); }, [name]);
  이렇게 하면 name의 값이 변경될 때마다 console.log 가 실행됩니다.

  3. useRef : 컴포넌트에 참조값을 설정하고, 참조하기 위한 hook 입니다.
  const refUid =useRef(); 로 ref 를 생성하고 이렇게 하면 입력한 값을 참조할 수 있습니다.

  4. useSearchParams :스프링의 @requestParam 어노테이션처럼 url의 쿼리 매개변수에 접근할 때 사용합니다.
  예를 들어 let [searchParams, setSearchParams] = useSearchParams(); let name = searchParams.get('name'); 이렇게 하여 url 쿼리 매개변수에서 name 의 값을 얻을 수 있습니다.


  5. useLocation :현재 url에 대한 정보에 접근하기 위한 hook입니다.

  6. useNavigate : 자바스크립트의 window.location.href 와 비슷한 역할을 합니다. 이 프로젝트에서는 사용자가 로그인을 하지 않았는데 채팅으로 접속을 시도 할 경우 alert("로그인 후 사용해주세요.")   이후 useNavigate를 이용해 login 화면으로 이동시킬 때 사용하였습니다.

</details>



✏️ Socket 통신을 이해하게 되었습니다. 또한 파일 전송과 일반 문자 전송을 어떻게 구분할 지 생각하면서 사고력이 증가되었습니다.
그리고 실시간 알람을 모든 페이지에서 확인 할 수 있도록, socket을 생성하고, 이를 모든 페이지에 주입시켜 하나의 socket으로 여러 곳에서 사용가능 하도록 구현하는 법을 알 수 있었습니다.
<details>
  <summary>학습한 socket 통신 </summary>
  <br>
  
  webSocket이란 서버와 클라이언트 간의 메시지 교환을 위한 통신규약을 말합니다. 양방향 통신이 가능하며, http와 다르게 지속적 연결을 수립하여 실시간 데이터 처리를 요하는 작업에 유용하게 쓰입니다.
구현한 과정

1. implementation 'org.springframework.boot:spring-boot-starter-websocket' 로 스프링에 의존성을 주입합니다.
2. TextWebSocketHandler를 상속하는 SocketHandler class를 작성하여, 소켓 연결, 소켓 종료, 메시지 발송 메소드를 작성합니다.
3. WebSocketConfigurer를 구현한 WebSocketConfig class를 작성합니다. 요청과 생성한 handler를 연결시켜 줍니다.
4. 프론트(react)에서 ws = new WebSocket("ws://요청 주소")로 소켓을 생성합니다.
</details>






