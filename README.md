# Character iPhone · 17 Pro 스타일

소설 독자를 위한 **가상 아이폰 웹사이트**입니다. 실제 iOS나 Apple의 공식 사이트는 아닙니다.

## Vercel 배포 (코딩 없이)
1. GitHub 계정을 만들고 새 저장소(repository)를 만듭니다.
2. 이 폴더의 `index.html`, `style.css`, `app.js`, `content.json` 파일을 저장소 최상위에 업로드합니다.
3. https://vercel.com 에 GitHub로 로그인하고 **Add New → Project**를 선택합니다.
4. 해당 저장소를 **Import**합니다. Framework Preset은 **Other**, Build Command는 비워 두고 **Deploy**를 누릅니다.
5. 배포된 `*.vercel.app` 주소를 소설에 넣으면 됩니다.

## 내용 수정
- 사이트 오른쪽 상단 **작가 편집**을 누르고 이름·배경화면·JSON 데이터를 수정합니다.
- **미리보기 적용**으로 테스트한 후 **JSON 다운로드**를 누릅니다.
- 내려받은 `content.json` 파일을 GitHub 저장소의 기존 `content.json`과 교체하고 변경 사항을 Commit합니다.
- Vercel이 자동 재배포합니다. (연결 및 자동 배포 설정에 따라 다를 수 있음.)

### JSON 데이터 형식
- `contacts`: `{ "id":"yeoju", "name":"여주", "phone":"010-0000-0000" }`
- `messages`: `{ "contactId":"yeoju", "items":[{"from":"me", "text":"안녕"},{"from":"them", "text":"응"}] }`
- `notes`: `{ "title":"제목", "body":"내용" }`
- `photos`: `{ "url":"https://example.com/photo.jpg", "caption":"사진 설명" }`
- `wallpaper`: 공개 HTTPS 이미지 주소. 이미지 서버가 외부 표시를 허용해야 합니다.

**주의:** 편집 화면은 로그인으로 보호된 관리자 페이지가 아닙니다. 링크를 아는 방문자도 편집 버튼을 볼 수 있지만, 편집한 내용은 자신의 브라우저에만 임시 저장됩니다. 공개 사이트 내용을 바꾸려면 저장소 접근 권한이 필요합니다. 실명·실제 전화번호·민감정보는 넣지 마세요.

## 기능 및 한계
잠금화면, 홈, 메시지, 사진, 연락처, 메모, 전화 목록 형태, 설정 화면이 있습니다. 전화 걸기·문자 전송은 작동하지 않습니다. 아이콘과 화면은 iOS 스타일을 참고해 직접 구현한 것이며 실제 Apple 아이콘·OS의 정확한 복제품은 아닙니다.
