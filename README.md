# 모두의진학 · 생기부 면접 분석

학교생활기록부 PDF를 올리면 **탐구 주제 · 개념어 · 읽은 책**을 목록으로 세우고, 목록에서 누르면 **생기부 원문의 그 쪽**이 바로 열리는 학생부종합전형 면접 준비 도구입니다.

파일은 브라우저 안에서만 처리되며 어디로도 전송되지 않습니다.

---

## 올리는 법 (5분)

1. 깃허브에서 새 저장소를 만듭니다. 이름은 예를 들어 `saenggibu` 로 합니다. **Public** 으로 만들어야 GitHub Pages가 무료로 동작합니다.
2. 저장소 화면에서 **Add file → Upload files** 를 누르고, 이 폴더의 파일 네 개를 그대로 끌어다 놓습니다.
   - `index.html`
   - `og-image.png`
   - `.nojekyll`
   - `README.md`
3. 아래 **Commit changes** 를 눌러 저장합니다.
4. 저장소 **Settings → Pages** 로 갑니다. `Source` 를 **Deploy from a branch**, `Branch` 를 **main / (root)** 로 두고 Save 합니다.
5. 1~2분 뒤 같은 화면 위쪽에 주소가 뜹니다.

```
https://<내아이디>.github.io/<저장소이름>/
```

예를 들어 아이디가 `moduui`, 저장소가 `saenggibu` 라면 주소는 이렇게 됩니다.

```
https://moduui.github.io/saenggibu/
```

---

## 링크 썸네일 (카카오톡·문자로 보낼 때)

카톡이나 SNS에 주소를 붙여 넣었을 때 미리보기 그림이 뜨게 하려면, `index.html` 안의 주소 세 줄을 **내 주소로 바꿔야 합니다.** 파일 맨 위쪽에 이렇게 표시해 두었습니다.

```html
<!-- ▼▼ 깃허브에 올린 뒤 아래 3줄의 주소만 내 저장소 주소로 바꿔 주세요 ▼▼ -->
<meta property="og:url"     content="https://USERNAME.github.io/REPO/">
<meta property="og:image"   content="https://USERNAME.github.io/REPO/og-image.png">
<meta name="twitter:image"  content="https://USERNAME.github.io/REPO/og-image.png">
<!-- ▲▲ 여기까지 ▲▲ -->
```

`USERNAME` 과 `REPO` 두 군데만 내 것으로 고치면 됩니다. 위 예시라면 이렇게 됩니다.

```html
<meta property="og:url"     content="https://moduui.github.io/saenggibu/">
<meta property="og:image"   content="https://moduui.github.io/saenggibu/og-image.png">
<meta name="twitter:image"  content="https://moduui.github.io/saenggibu/og-image.png">
```

고치는 방법은 저장소에서 `index.html` 을 누른 뒤 연필 모양(Edit) 아이콘 → `Ctrl+F` 로 `USERNAME` 검색 → 수정 → Commit 입니다.

주소를 바꾼 뒤에도 예전 미리보기가 계속 뜨면 캐시 때문입니다. 카카오톡은 [개발자 도구의 캐시 초기화](https://developers.kakao.com/tool/clear/og), 페이스북은 [공유 디버거](https://developers.facebook.com/tools/debug/)에서 주소를 넣고 새로 읽어오면 됩니다.

---

## 안전에 관하여

- 생활기록부 PDF는 **브라우저 메모리 안에서만** 열립니다. 서버로 보내는 코드가 없습니다.
- 분석에 필요한 프로그램(PDF 판독기 포함)이 `index.html` 한 파일 안에 모두 들어 있어 **외부 인터넷을 전혀 쓰지 않습니다.** 인터넷을 끄고 열어도 똑같이 동작합니다.
- 페이지에 **Content-Security-Policy** 를 걸어 `connect-src 'none'` 으로 두었습니다. 코드가 실수로든 고의로든 **바깥으로 데이터를 보내려 해도 브라우저가 막습니다.**
- 외부 스크립트, 광고, 분석 도구, 쿠키, 로컬 저장소를 일절 쓰지 않습니다.
- 이름·학교·주민등록번호·주소·연락처는 기본으로 가려서 표시합니다. 체크를 풀면 원래대로 보입니다.
- 탭을 닫으면 읽어 들인 내용은 즉시 사라집니다.

> 다만 **생기부 원문 보기** 화면은 올린 PDF를 그대로 그려 보여 주므로 이름과 사진이 보입니다. 공용 PC나 화면 공유 중에는 주의해 주세요.

---

## 쓰는 법

| 화면 | 하는 일 |
|---|---|
| **면접 포인트** | 왼쪽은 기록 목록, 오른쪽은 상세. 목록 제목은 본문이 아니라 **뽑아낸 주제**라 훑기만 해도 걸리는 게 보입니다. |
| **학기별 흐름** | 1학년 1학기부터 쌓인 순서대로. 본문에 주제(노랑)·개념어(청록)·책(보라)이 칠해집니다. |
| **탐구 주제** | 전체 주제를 학기 순으로 모은 표. 줄을 누르면 그 기록으로 갑니다. |
| **개념어** | 많이 나온 순 / 학년별 / 학기별 / 과목·영역별로 나누어 봅니다. |
| **독서** | 독서활동상황과 본문에 언급된 책을 학년별로. |

위쪽 검색창에 단어를 넣으면 다섯 화면이 한꺼번에 걸러집니다. 학년·영역·밀도 단추로도 좁힐 수 있습니다.

**면접 준비 노트 인쇄**를 누르면 학기별 기록(메모 줄 포함), 개념어 설명 연습표, 독서 정리로 이루어진 인쇄물이 나옵니다.

---

## 알아 둘 점

- 나이스에서 내려받은 **학교생활기록부 II** 출력본을 권장합니다. 스캔한 이미지 PDF는 글자가 없어 읽지 못합니다.
- 학교마다 표 모양이 조금씩 달라 판독이 어긋날 수 있습니다. 면접에 쓰기 전에 **원문 보기**로 한 번 대조해 주세요.
- 자동 추출은 보조 도구입니다. 판단은 사람이 합니다.

---

Copyright © 모두의진학 (All Teachers). 진학의 정보를, 모두에게.
