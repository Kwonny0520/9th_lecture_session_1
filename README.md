🚀 GitHub 실습 및 과제 제출 가이드
## 👥 동아리 부원 목록

아래 링크를 클릭하면 부원들의 방명록을 볼 수 있습니다!

{% for page in site.pages %}
  {% if page.path contains 'members/' %}
  - [👉 {{ page.title }} 님의 방명록 보기]({{ site.baseurl }}{{ page.url }})
  {% endif %}
{% endfor %}

## 📌 실습 개요
본 저장소는 **학술동아리** 신입 부원 및 프로젝트 팀원들을 위한 **Git/GitHub 온보딩 실습 공간**입니다. 
협업의 핵심인 **Fork, Clone, Branch, Commit, Push, Pull Request(PR)**의 전체 프로세스를 직접 경험하며 GitHub를 통한 협업 흐름을 익히는 것을 목표로 합니다.

우리는 이번 실습을 통해 동아리 부원들의 한 줄 소개가 담긴 **방명록(`members.md`)**을 함께 완성해 볼 예정입니다.

---

## 🛠️ 사전 준비
실습을 시작하기 전, 아래 두 가지가 준비되어 있어야 합니다.
1. **GitHub 계정 생성**
2. **Git 설치 및 개발 환경 세팅** (아래 중 본인에게 편한 방법을 선택하세요)
   - 터미널/CLI 환경: [Git 공식 다운로드](https://git-scm.com/)
   - GUI 툴 환경: [GitHub Desktop 다운로드](https://desktop.github.com/) 또는 **VS Code (Visual Studio Code)**

---

## 🏃‍♂️ 실습 진행 단계 (Fork & PR 워크플로우)

차근차근 아래의 단계를 따라와 주세요. 처음이라 낯설더라도 하나씩 해결하다 보면 금방 익숙해질 수 있습니다!

### 1단계. 저장소 복사하기 (Fork)
1. 본 리포지토리 우측 상단에 있는 **[Fork]** 버튼을 클릭합니다.
2. Owner를 본인의 개인 계정으로 선택한 뒤, **[Create fork]**를 누릅니다.
3. 이제 본인의 개인 GitHub 계정 아래에 동일한 이름의 복사본 저장소가 생성됩니다.

### 2단계. 내 컴퓨터로 가져오기 (Clone)
1. Fork된 **본인 소유의 GitHub 저장소**로 이동합니다. (인터넷 주소창에 동아리 계정이 아닌 본인의 GitHub 아이디가 포함되어 있는지 꼭 확인하세요!)
2. 초록색 **[<> Code]** 버튼을 누르고, **HTTPS** 탭에 있는 URL 주소를 복사합니다.
3. 컴퓨터에서 에디터(VS Code) 또는 GitHub Desktop을 열고, 복사한 주소를 사용하여 프로젝트를 **Clone(다운로드)** 합니다.
   - *VS Code의 경우:* `Ctrl + Shift + P` (Mac은 `Cmd + Shift + P`) -> `Git: Clone` 입력 -> 주소 붙여넣기

### 3단계. 나만의 작업 공간 만들기 (Branch)
메인 코드를 안전하게 보존하면서 나만의 작업을 독립적으로 하기 위해 새로운 '가지(Branch)'를 만들어야 합니다.
- 브랜치 이름 규칙: `add-member-[본인영어이름]` (예: `add-member-gildong`)
- *VS Code의 경우:* 좌측 하단의 브랜치 표시(기본값 `main`)를 누르거나, 소스 제어 탭에서 `...` -> `Branch` -> `Create Branch`를 선택하여 새 브랜치 이름을 입력합니다.

### 4단계. 방명록 작성하기 (Edit & Commit)
1. 프로젝트 폴더 내에 있는 **`members.md`** 파일을 엽니다.
2. 파일의 맨 아래에 예시 양식에 맞추어 본인의 정보를 추가하고 저장(`Ctrl + S` / `Cmd + S`)합니다.
3. VS Code 좌측의 소스 제어(Source Control) 탭(나뭇가지 모양 아이콘)으로 이동합니다.
4. 변경된 members.md 파일 옆의 + (Stage Changes) 버튼을 누릅니다.
5. 상단 입력창에 어떤 작업을 했는지 명확히 적고(예: feat: 홍길동 방명록 추가), [Commit] 버튼을 누릅니다.
+ Github Desktop을 쓰는 경우, 왼쪽 Changes 창에 상태 변화가 뜨는 것을 확인 후, 아래 Commit Summary & Description을 작성한 후 Commit 버튼을 누릅니다.

### 5단계. 내 GitHub에 올리기 (Push)
- 커밋한 내용을 인터넷에 있는 본인의 Fork 저장소로 업로드합니다.
- VS Code 소스 제어 탭의 [Publish Branch] 또는 [Sync Changes] 버튼을 눌러 Push를 완료합니다.

### 6단계. 동아리 원본 저장소로 반영 요청하기 (Pull Request)
1. Push를 마치고 다시 동아리 원본 GitHub 저장소로 접속합니다.
2. 화면 상단에 초록색 [Compare & pull request] 버튼이 활성화되어 있는 것을 볼 수 있습니다. 버튼을 클릭합니다.
3. PR 제목과 내용을 확인한 뒤, 우측 하단의 [Create pull request] 버튼을 누르면 과제 제출이 완료됩니다! 🎉

⚠️ 자주 발생하는 문제 & 대처법 (Merge Conflict)
여러 부원이 동시에 같은 파일의 같은 위치를 수정하기 때문에, 내 PR 화면에 "Can't automatically merge"라는 경고와 함께 병합 충돌(Conflict)이 발생할 수 있습니다. 이는 아주 자연스러운 현상이며, 협업 과정에서 반드시 배워야 할 필수 관문입니다!

💡 해결 방법 (GitHub 웹 UI에서 해결하기)
본인이 올린 PR 페이지로 이동합니다.

화면 하단 충돌 경고 옆에 있는 [Resolve conflicts] 버튼을 클릭합니다.

에디터 화면에 표시된 <<<<<<<, =======, >>>>>>> 기호 사이의 텍스트를 확인합니다.

기존에 다른 사람이 작성한 내용과 내가 새로 추가한 내용이 둘 다 안전하게 유지되도록 불필요한 Git 기호들을 지우고 줄바꿈을 보기 좋게 정돈합니다.

정리가 끝났다면 우측 상단의 [Mark as resolved] -> [Commit merge]를 차례로 누릅니다.

다시 초록색으로 변경된 상태(This branch has no conflicts with the base branch)를 확인하면 완료됩니다! 관리자가 확인 후 최종 병합(Merge)을 진행합니다.

💡 문의 사항이 있거나 진행 중 막히는 부분이 있다면 언제든 동아리 소통 창구나 관리자에게 편하게 질문해 주세요!