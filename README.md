# community-site-team3
(주)롯데정보통신 사내 커뮤니티 사이트 프로젝트

### 제작기간
--------------------------------------
2024.05.20 ~ 2024.06.21(1달)

### 프로젝트 개요
--------------------------------------
1. 프로젝트 주제 : 사내 커뮤니티, OrangeNode
2. 프로젝트 기간 : 2024-05-20 ~ 2024-06-21
3. 배경 및 목적 : 사내 커뮤니티를 개설해 보았습니다. 일정을 관리하고, project를 생성하고, 실시간 채팅을 통해 업무 효율화를 목적으로 합니다.
4. 담당한 기능: 채팅,게시판
5. 팀 구성 : 김선광, 정원구, 김형민, 정태영, 최이진


### 사용한 기술
--------------------------------------
Spring Boot, Java, REACT, HTML5/CSS3/JavaScript, MyBaits, JPA, AWS


### ERD
--------------------------------------
![image](https://github.com/Taeyoung20230727/OrangeNode-F/assets/140632598/82bb028e-10fd-4812-a51e-88ed07a29845)


# 직접 구현한 기능 영상
--------------------------------------
## 게시판
[![게시판 동영상](http://img.youtube.com/vi/awCfZnPH_Sc/maxresdefault.jpg)](https://youtu.be/awCfZnPH_Sc)

## 채팅
[![채팅 동영상](https://img.youtube.com/vi/GgoQ1-DBkQY/maxresdefault.jpg)](https://youtu.be/GgoQ1-DBkQY)

이 프로젝트를 통해 배운 내용

✏️ React의 여러 hook (useState, useEffect, useRef 등) 들을 직접 사용해보며 사용 목적과 사용 방법을 알게 되었습니다.
# React Hooks

<details>
  <summary>학습한 react hook 내용 (사용 목적, 사용 방법) [클릭]</summary>
  <br>

  1️⃣ useState : 컴포넌트의 상태값을 선언하고 관리하는 hook입니다. const [count, setCount] = useState(0); 식으로 초기 값을 0으로 선언할 수도 있고, const [list, setList] = useState([])로 빈 배열 형태로 선언할 수도 있습니다. 혹은 const [user, setUser ] = useState({uid:'', name:"", age:0}) 이렇게 원하는 빈 객체 값으로 선언할 수도 있습니다.

  2️⃣ useEffect : 의존성 배열을 이용해, 상태값이 업데이트 될 때마다 실행할 수 있습니다.
  useEffect(() => { console.log("state name update..."); }, [name]);
  이렇게 하면 name의 값이 변경될 때마다 console.log 가 실행됩니다.

  3️⃣ useRef : 컴포넌트에 참조값을 설정하고, 참조하기 위한 hook 입니다.
  const refUid =useRef(); 로 ref 를 생성하고 이렇게 하면 입력한 값을 참조할 수 있습니다.

</details>







