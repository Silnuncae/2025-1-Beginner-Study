
## 개발 입문 스터디 1주차 WIL

### 이번주 스터디 목표

Git과 GitHub에 대해 이해하고, Git을 이용하여 GitHub에 파일을 Push해보는 것

---

### Git이란 무엇이고 왜 필요한가?

실제로 개발을 하다 보면 수정된 코드가 많아지고,  
파일이 점점 복잡해지며 여러 사람이 동시에 작업해야 하는 상황이 온다.  

그래서 **Git을 사용**한다.

> Git은 개발자가 코드를 효율적으로 관리하고 협업할 수 있도록 도와주는 **버전 관리 도구**이다.

Git을 사용하면 다음이 가능하다:

- 어떤 파일이 수정되었는지
- 누가, 언제, 어떻게 바꿨는지
- 이전 버전으로 되돌리기

---

### Git의 기본 구조

| 구분 | 설명 |
|------|------|
| **Working Directory** | 현재 작업 중인 실제 파일 |
| **Staging Area**      | 커밋할 준비가 된 파일 |
| **Repository**        | Git이 이력을 저장하는 공간 |

---

### 1. Git 최초 설정

```bash
git config --global user.name "깃허브 이름"
git config --global user.email "깃허브 이메일"
```

> Git에게 내 GitHub 정보를 알려주는 설정

---

### 2. 디렉토리 만들기

원하는 위치에 새로운 폴더를 만들고,  
**VSCode에서 해당 폴더를 열어준다.**

---

### 3. Git으로 파일 관리하기

```bash
git init
```

> 현재 폴더를 Git으로 관리 가능한 저장소로 만들겠다는 명령어  
> 성공 시: `Initialized empty Git repository in <파일경로>` 메시지가 뜬다.

```bash
git add <파일명>
git add .
```

> 해당 파일 또는 폴더 내 모든 파일을 Staging Area에 추가

```bash
git commit -m "commit message"
```

> 커밋 메시지와 함께 Repository에 저장

---

### 커밋 메시지 타입 (Commit Message Type)

예시:  
```bash
git commit -m "docs: 1주차 개발 입문 스터디 wil.md 작성"
```

| 타입     | 의미                         |
|----------|------------------------------|
| `feat`   | 새로운 기능 추가             |
| `fix`    | 버그 수정                    |
| `refactor` | 코드 개선 (기능 변화 없음) |
| `chore`  | 설정, 환경 등 코드 외 변경   |
| `docs`   | 문서 작업                    |
| `test`   | 테스트 코드 작성 또는 수정   |

---

### 4. GitHub Repository와 연동하기

1. GitHub에 새 Repository 생성
2. 터미널에서 아래 명령어 실행:

```bash
git remote add origin https://github.com/유저명/레포명.git
git branch -M main
git push -u origin main
```

---

### 5. GitHub에 올리기

```bash
git add <파일명>
git commit -m "commit message"
git push origin main
```

---
