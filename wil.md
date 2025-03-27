## <개발 입문 스터디 1주차 WIL>

### 이번주 스터디 목표
Git과 GitHub에 대해 이해하고 Git을 이용하여 GitHub에 Push해보는 것


**Git이란 무엇이고 왜 필요한가

실제로 개발을 하다보면 수정된 코드가 많아지고
파일이 점점 복잡해지며 여러사람이 동시에 작업해야 하는 상황이 온다. 
그래서 Git을 사용한다.

Git은 개발자가 코드를 효율적으로 관리하고 협업할 수 있도록 도아주는 버전 관리 도구이다.

Git을 사용하면:
- 어떤 파일이 수정되었는지
- 누가 언제 어떻게 바꿨는지
- 이전 버전으로 되돌릴지
가 가능해진다.

**Git의 기본 구조

Working Directory : 현재 작업 중인 실제 파일
Staging Area : 커밋할 준비가 된 파일
Repository : Git이 이력을 저장하는 공간

**1. Git 최초 설정

git config --global user.name "깃허브 이름"
git config --global user.email "깃허브 이메일"
-> Git에다가 내 Github의 정보를 넣어주는 설정

**2. 디렉토리 만들기
원하는 위치에 새로운 폴더를 만들고 VSCode에서 폴더를 열어준다.

**3. Git으로 파일 관리하기
git init
-> Initialized empty Git repository in '파일경로'가 뜨면 성공
-> 현재 폴더를 Git 저장소로 만드는 명령어

git add "파일명"
git add .
-> 변경된 파일을 Staging Area에 올리는 명령어 

git commit -m "commit message"
-> 커밋 메시지랑 같이 Repository에 저장하는 명령어

**Commit Message Type

ex) docs : 1주차 개발 입문 스터디 will.md

feat : 새로운 기능을 추가 했을 때
fix : 버그를 수정했을 때
refactor : 코드를 개선했을 때
chore : 코드 외 설정, 환경을 변경했을 때
docs : 문서를 올렸을 때
test : 테스트 코드

**4. Github의 해당 Repository와 연동하기

먼저 Github에 새로운 Repository를 만든다.

git remote add origin https://github.com/유저명/레포명.git
-> Repository의 주소이다.
git branch -M main
git push -u origin main

**5. Github에 올리기

git add <파일명>
git commit -m “commit message”
git push origin main

