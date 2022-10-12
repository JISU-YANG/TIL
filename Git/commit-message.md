
### 메시지 구조
```
type(옵션): [#issueNumber - ]Subject // 제목
(한 줄을 띄워 분리한다.)

body(옵션) // 본문
(한 줄을 띄워 분리한다.)

footer(옵션) // 꼬리말
``` 

### 메시지 타입
- Feat: 기능 추가
- Fix: 버그 수정
- Design: UI 변경
- Style: 코드 스타일 관련 수정
- Refactor: 코드 리팩토링
- Comment: 주석 변경
- Docs: 문서 수정
- Test: 테스트 수정
- Rename: 파일명, 폴더명 수정 및 이동
- Remove: 파일 삭제

### 메시지 규칙
1. 첫 글자는 대문자로 작성
2. 명령어로 시작 ("Fix", "Add", "Change")
```
예) Feat: "추가 get data api 함수"
```