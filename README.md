# wifi-web
내 위치 가반 공공 와이파이 정보제공을 위한 웹 서비스

- 활용기술
    - Java 8.x
    - JSP
    - MariaDB 11.1.2
    - docker v4.23.0
    - docker-compose v2.21.0

1. RDBMS 환경 구성  
    - docker 및 docker-compose 를 설치한다.  
    - $ docker-compose up -d 수행 한다.  
    - .env 파일을 확인하여 localhost 로 디비를 접속 한다.
    - 디비 툴로 접속 후 **내 위치 기반 공공 와이파이.sql** 열어서 테이블을 생성한다.
      
2. 이클립스에서 Web Server 구성
   - java 8 이상 버전 설치
   - tomcat 9.0 이상 버전 설치
   - 이클립스에서 프로젝트 추가 후 서버 기동

3. 화면 메뉴 설명
   - http://localhost:8080/home.jsp 로 접속
   - Open API 와이파이 정보 가져오기 : 공공 와이파이 정보를 가져온다.
   - 홈 : "내 위치 가져오기" 버튼 클릭 후 "근처 WIFI 정보 보기" 버튼을 클릭 한다.
       - 와이파이명 선택 시 상세화면으로 이동 한다.
       - 북마크 추가 하기 전에 북마크 그룹 메뉴에서 그룹 추가 후 수행한다.
   - 위치 히스토리 목록 : 홈 에서 검색시 내 위치 검색을 기록한다.
   - 북마크 보기 : 북마크 목록을 조회, 삭제 한다.
   - 북마크 그룹 관리 : 북마크 그룹을 추가, 삭제, 수정 한다. 
