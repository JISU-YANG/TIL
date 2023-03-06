### 기본 명령어
- ls : 목록조회
- ls-al : 숨긴 파일 포함 목록 조회
- cd : 디렉터리 이동
- rm : 파일 지우기
- rm-rf: 폴더 지우기
 
### 프로젝트 연결
- git init
    - 현재 경로에 초기화한다.
- git remote add origin master [url]
    - 저장소를 연결한다.
    - 연결확인 git remote -v
- git add .
    - 전체를 스테이지에 올린다.
- git commit
    - 스테이지를 커밋한다.
- git push origin master
    - 커밋들을 푸시한다.
 

### Git 명령어
- git status
    - 변경된 파일 조회
- git log
    - 커밋 로그 조회
- git log --graph
    - 커밋 로그 시각화 조회