## 🚀 GitHub 실습 및 과제 제출 가이드
### 👥 동아리 부원 목록
아래 링크를 클릭하면 부원들의 방명록을 볼 수 있습니다!

{% for page in site.pages %}
  {% if page.path contains 'members/' %}
  - [👉 {{ page.title }} 님의 방명록 보기]({{ site.baseurl }}{{ page.url }})
  {% endif %}
{% endfor %}

## 📌 실습 개요
본 저장소는 학술동아리 신입 부원 및 프로젝트 팀원들을 위한 Git/GitHub 온보딩 실습 공간입니다.
협업의 핵심인 Fork, Clone, Branch, Commit, Push, Pull Request(PR)의 전체 프로세스를 직접 경험하며 GitHub를 통한 협업 흐름을 익히는 것을 목표로 합니다.

우리는 이번 실습을 통해 members/ 폴더에 각자의 프로필 마크다운 파일을 추가하여 동아리 부원 전체의 방명록 웹사이트를 함께 완성해 볼 예정입니다.

--- 

## 🛠️ 사전 준비
실습을 시작하기 전, 아래 두 가지가 준비되어 있어야 합니다.

GitHub 계정 생성

Git 설치 및 개발 환경 세팅 (아래 중 본인에게 편한 방법을 선택하세요)

터미널/CLI 환경: Git 공식 다운로드

GUI 툴 환경: GitHub Desktop 다운로드 또는 VS Code (Visual Studio Code)

--- 

## 🏃‍♂️ 실습 진행 단계 (Fork & PR 워크플로우)
차근차근 아래의 단계를 따라와 주세요. 처음이라 낯설더라도 하나씩 해결하다 보면 금방 익숙해질 수 있습니다!

### 1단계. 저장소 복사하기 (Fork)
- 본 리포지토리 우측 상단에 있는 [Fork] 버튼을 클릭합니다.
- Owner를 본인의 개인 계정으로 선택한 뒤, [Create fork]를 누릅니다.
- 이제 본인의 개인 GitHub 계정 아래에 동일한 이름의 복사본 저장소가 생성됩니다.

### 2단계. 내 컴퓨터로 가져오기 (Clone)
- Fork된 본인 소유의 GitHub 저장소로 이동합니다. (인터넷 주소창에 동아리 계정이 아닌 본인의 GitHub 아이디가 포함되어 있는지 꼭 확인하세요!)
- 초록색 [<> Code] 버튼을 누르고, HTTPS 탭에 있는 URL 주소를 복사합니다.
- 컴퓨터에서 에디터(VS Code) 또는 GitHub Desktop을 열고, 복사한 주소를 사용하여 프로젝트를 Clone(다운로드) 합니다.
- VS Code의 경우: Ctrl + Shift + P (Mac은 Cmd + Shift + P) -> Git: Clone 입력 -> 주소 붙여넣기
- 💡 주의: GitHub Desktop에서 Clone 할 때 목적을 묻는 창이 뜨면, 반드시 **'To contribute to the parent project (상위 프로젝트에 기여)'** 를 선택해 주세요!

### 3단계. 나만의 작업 공간 만들기 (Branch)
- 메인 코드를 안전하게 보존하면서 나만의 작업을 독립적으로 하기 위해 새로운 '가지(Branch)'를 만들어야 합니다.
- 브랜치 이름 규칙: add-member-[본인영어이름] (예: add-member-gildong)
- **VS Code**의 경우: 좌측 하단의 브랜치 표시(기본값 main)를 누르거나, 소스 제어 탭에서 ... -> Branch -> Create Branch를 선택하여 새 브랜치 이름을 입력합니다.
- **Github Desktop**의 경우: 상단의 Current Branch를 눌러 

### 4단계. 나만의 프로필 파일 만들기 (Create & Commit)
- 프로젝트 폴더 내에 있는 members 폴더로 이동합니다.
- members 폴더 안에 [본인영어이름].md 파일의 형태로 새로운 파일을 생성합니다. (예: gildong.md)
- 새 파일 최상단에 웹사이트 빌드를 위한 Front Matter(제목 설정)를 반드시 포함하여 아래 양식에 맞추어 정보를 작성하고 저장합니다.
- 에디터나 GUI 도구에서 변경 사항을 확인하고 스테이징(Stage) 후 커밋을 진행합니다.
- **VS Code**의 경우: 좌측 소스 제어 탭에서 생성된 파일 옆의 + 버튼을 누르고, 상단 입력창에 커밋 메시지(예: feat: 홍길동 프로필 추가)를 적은 후 [Commit]을 누릅니다.
- **GitHub Desktop**의 경우: 왼쪽 Changes 창에 내 파일이 추가된 것을 확인하고, 좌측 하단의 Summary에 메시지를 작성한 뒤 [Commit to ...] 버튼을 누릅니다.

### 5단계. 내 GitHub에 올리기 (Push)
- 커밋한 내용을 인터넷에 있는 본인의 Fork 저장소로 업로드합니다.
- VS Code 소스 제어 탭의 [Publish Branch] 또는 [Sync Changes] 버튼을 누르거나, GitHub Desktop 상단의 [Publish branch] 버튼을 눌러 Push를 완료합니다.

### 6단계. 동아리 원본 저장소로 반영 요청하기 (Pull Request)
- Push를 마치고 다시 동아리 원본 GitHub 저장소로 접속합니다.
- 화면 상단에 초록색 [Compare & pull request] 버튼이 활성화되어 있는 것을 볼 수 있습니다. 버튼을 클릭합니다.
- PR 제목과 내용을 확인한 뒤, 우측 하단의 [Create pull request] 버튼을 누르면 과제 제출이 완료됩니다! 🎉

#### 🔄 과제 제출 후 내 저장소 최신화하기 (Sync Fork)
- 동아리 원본 저장소에 내 코드가 최종 병합(Merge)되거나 다른 부원들의 과제가 반영되더라도, 본인의 개인 GitHub 저장소(Fork)와 컴퓨터에 있는 로컬 코드는 자동으로 업데이트되지 않습니다. 
- 다음 실습이나 프로젝트를 진행하기 위해 아래 방법으로 저장소를 최신 상태로 유지해 주세요.

#### 💡 동기화 방법
- 본인의 GitHub 계정에 있는 Fork된 저장소 페이지로 이동합니다.
- 메인 화면 중간에 있는 [Sync fork] 버튼을 누르고, [Update branch]를 클릭합니다. (동아리 원본의 최신 상태가 내 GitHub로 동기화됩니다.)
- 컴퓨터에서 VS Code나 GitHub Desktop을 열고 브랜치를 main으로 변경(Checkout)한 뒤, [Pull] 또는 [Sync Changes]를 눌러 최신 코드를 다운로드합니다.

### 💡 문의 사항이 있거나 진행 중 막히는 부분이 있다면 언제든 동아리 소통 창구나 관리자에게 편하게 질문해 주세요!