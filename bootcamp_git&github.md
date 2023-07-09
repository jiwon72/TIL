# bootcamp TIL

## git&github

### git

---

- 여러명의 개발자가 하나의 소프트 웨어 개발 프로젝트에 참여할때 소스코드를 관리해야할때 사용된다
- 최종 최최종 최최최종 진짜최종 만들때
- **소스코드 버전 관리**

### github

- git을 올리는 사이트

#### git 용어

- Repository : 저장소, 모든 히스토리 확인 가능
- Commit : 현재 변경된 작업 상태를 점검을 마치면 확정하고 저장소에 저장
- Branch : 가지
- Merge : 다른 Branch의 내용을 현재 Branch로 가져와 합치는 작업

#### git 기본 명령어

- git help : 도움말
- git init : 깃 저장소 초기화
- git status : 저장소 상태체크
- git branch : 새로운 브랜치 생성
- git add : 변경내용 추가
- git push : 컴퓨터에서 서버로 변경사항 "push"
- git pull : 저장소로부터 최신버전 "pull"
- git clone : 저장소의 데이터를 컴퓨터로 복사
- git merge : 개별 브랜치에서 마친 작업을 master 브랜치로 병합

### github올리는 법

1. terminal -> new terminal
2. git init
3. git add . (git add 파일명 해도돼) (. = all)
4. git status (상태확인)
5. git commit –m “first commit” (first commit : 히스토리명)
6. git remote add origin https://github.com/jiwon72/-.git

### 원래 올린것에 추가하고 싶을때

1. git add .
2. git status
3. git commit –m “second commit”
4. git push origin master (깃허브로 올리기)

### 여러가지

- 깃삭제 : rm –rf.git
- 명령어 줄이기 : alias
- 소스코드 다운로드 :
  git clone 주소 폴더이름
- Markdown 찾아보기
