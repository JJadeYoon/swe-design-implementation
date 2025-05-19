# <과제 2 : Design & Implementation – 공유 자전거 대여 시스템>

## 1. 개요

아래 수정된 과제 명세서의 requirement 변경 사항을 반영하여 requirement capturing을
다시 수행한다. 이에 따라 도출된 결과물을 기반으로 requirement analysis 단계를 수행한다.
마지막으로 detailed design과 implementation을 수행한다. 메뉴 및 파일입출력 형식은 첨부된 파일
을 참고한다.

## 2. 수정된 기능

- 회원 가입 기능
시스템을 이용하려면 사용자는 회원 가입을 해야 한다. 회원의 필수 입력 정보는 ID, 비밀번호, 전화
번호~~, 전화번호, 결제 수단, 선호 자전거 유형(일반/전기) 등,~~이다. 관리자는 주어진 ID(admin)와 비밀
번호(admin)으로 로그인한다.
- 로그인/로그아웃 기능
관리자와 회원은 ID와 비밀번호로 로그인하며, 로그아웃 시 시스템 접속이 종료된다.
- 자전거 등록~~/조회/삭제~~ 기능
관리자는 자전거 정보를 등록, ~~조회 및 삭제~~할 수 있다. 등록 시 입력 정보는 자전거 ID, 자전거 제품명~~, 유형(일반/전기), 소속 대여소, 상태(사용 가능/수리 중) 등이다. 등록된 자전거 리스트를 조회할 수 있으며 원하는 자전거 항목을 선택해서 상세내용을 볼 수 있다. 또한, 등록된 자전거 리스트 조회 화면에서 특정 자전거 항목을 삭제할 수 있다.~~
- 자전거 대여 기능
회원은 특정 자전거를 대여할 수 있다.
- 자전거 대여 정보 조회
회원이 현재 대여 중인 자전거를 조회하면 해당 리스트가 출력되고 각 항목에는 ~~대여소 이름, 대여소 위치,~~ 자전거 ID, 자전거 제품명, ~~자전거 유형~~를 보여준다.

### 3. 과제 제출물

### 3.1 Requirement analysis

교재 Case Study A3를 참조하여 다음 documents를 작성해서 총 파일 6개를 압축해
서 제출함. 모든 압축파일은 자신의 학번, 이름을 파일 이름으로 만들기 바람

(예: b123456_홍길동.zip).
(https://books.google.co.kr/books?id=lMovEAAAQBAJ&lpg=PA169&hl=ko&pg=PA225#v=onepage&q&f=false)

1. 수정된 Requirement list(functional requirement만 명시함)
2. 수정된 use case diagram(UML tool 형식을 pdf 파일로 변환해서 제출)
3. 수정된 use case descriptions (step by step breakdown)
4. Communication diagram
5. Analysis class diagram
    
    association
    
6. 개인별 git commit history 파일 1개
    
    $ git log --pretty=“[%an] %cd %s %h” > log_output.txt
    
    ※ 위의 1>번 파일 첫 부분에 채점내용 공개용 개인코드와 개인 GitHub 주소를 명시하기
    바람.
    

### 3.1 Detailed design & implementation

2개의 과제 항목에 각각 제출해야 함

(2-1) 총 파일 2개를 압축해서 제출함.

1> 수정된 communication diagram

2> Design class diagram

- attribute type
- operation signature
- visibility (+, -, #, ~)
- association (collection class 등)

(2-2) 소스 코드 파일들(.cpp 및 .h 파일들만)

- 솔루션 파일(*.sln), 실행 파일(*.exe), 혹은 해당 폴더 전체를 제출하면 감점 처리함. 폴더를 포함해서 압축하지 말 것
- 채점을 위해 인코딩 및 한글 깨짐 문제를 방지하기 위해 반드시 Visual Studio
Community 2022 버전에서 컴파일되어 동작하는지 확인 바람.
※ coding convention 정보(예시: https://google.github.io/styleguide/cppguide.html,
[https://del4u.tistory.com/92에서](https://del4u.tistory.com/92%EC%97%90%EC%84%9C) Comments 섹션)를 참고해서 각 file, class,
operation, attribute의 naming & comment 형식을 결정해서 작성함

## 4. 제출 마감 시간 및 방법

1. 1차 제출 (requirement analysis)
    - 제출 마감 시간 : 5월 20일 (화요일) 오후 2시
    - 방법 : 클래스룸 ’과제2-1‘에 업로드
2. 최종 제출 (detailed design & implementation)
    - 제출 마감 시간 : 5월 27일 (화요일) 오후 2시
    - 방법 : 클래스룸 ’과제2-2-1‘(보고서)’ 및 ’과제2-2-2‘(소스코드)’에 각각 업로드
3. 유의 사항
    
    (1) 감점 사항
    
    - 기말고사 일정을 고려해서 이번 과제는 최종 제출 기한 이후에 하루만 지연 제출 허용
    함(25점 감점).
    - 부정행위 발견 시 관련 학생 모두 F 학점 처리함
    
    (2) 질문은 클래스룸 QnA 게시판을 이용하기 바람.
    

## 4. 채점 기준

1. 요구사항/기능이 모두 구현될 수 있도록 modeling 되었고 구현이 modeling과 일치하는가? (60점)
    
    
    |  | 체크 항목 | 감점 |
    | --- | --- | --- |
    | 1 | class, operation, attribute의 설계 내용이 구현 내용과 다른 경우  | 개당 –4점
    최대 -48점 |
    | 2 | boudnary class와 control class가 stereotype에 맞게 동작하는가? | 1개 이상 –12점
    (단일점수 감점) |
2. 프로그램이 데모 시나리오를 만족하는가? (30점)
    
    
    |  | 체크 항목 | 감점 |
    | --- | --- | --- |
    | 1 | 컴파일 에러
    (일부 소스 파일 미제출 등 제출자의 잘못인 경우 재채점은 불가함) | -30점 |
    | 2 | 각 입력에 대해 실행 결과가 틀린 경우
    (위의 1번 항목과 중복 감점하지 않음) | 개당 –3점
    최대 -30점 |
3. Source code가 convention에 따라 작성되었는가? (10점)
    
    
    |  | 체크 항목 | 감점 |
    | --- | --- | --- |
    | 1 | comment, class 이름, operation 이름을 작성하는 기준이 일관되지 않은 경우 | 1개 이상 –4점
    (단일점수 감점) |
    | 2 | comment를 작성하지 않은 경우 (class, operation)  | 개당 –2점
    최대 -6점 |