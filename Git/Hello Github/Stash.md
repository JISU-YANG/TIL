[Today I Learned](/README.md) > [Hello, Github](/Git/Hello%20Github/README.md) > Stash

---

</br>

# Stash

### 스태시(Stash)
현재 브랜치에서 커밋되지 않은 변경사항이 존재하지만 다른 브랜치로 체크아웃할 수 있도록 하는 임시 저장소이다.

### 스태시(Stash)의 특징
- 불필요한 커밋을 줄여줄 수 있다.
- git push --force 를 사용할 확률을 줄여준다.
- 변경된 내용을 스테이지에 올리지 않아도 진행할 수 있다.
- Untracked File(Git에 한번도 올라가지 않은 파일)은 스테이지에 올려줘야 한다.
- 이전 커밋 덮어쓰기도 가능하다.