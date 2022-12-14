<h1> Quest 00. 데브옵스란 무엇인가?. </h1>

<h2>Checklist</h2>

- 만약 비개발자에게 데브옵스가 무엇인지 설명하게 된다면 어떻게 설명할 수 있을까요?.
* A = 데브옵스(DevOps)는 개발(Development)과 운영(Operations)의 합성어이다. 개발과 운영의 경계를 허물고 하나의 팀으로서 소통, 협업 및 통합을 강조하는 개발 환경이나 문화를 뜻한다.

- 데브옵스라는 개념 이전의 소프트웨어 개발은 어땠을까요? 어떤 요구사항을 충족하기 위해 데브옵스라는 개념이 생겼을까요?
* A = 데브옵스 이전의 소프트웨어 개발 프로세스는 모든 단계에 걸쳐 사람이 개입(및 물리적 핸드오프)해야 하는 매우 수동적인 과정이었다. 사람이 개입해야 하는 이러한 프로세스로 인해 기업들은 1년에 한 번 새로운 코드를 업데이트하거나 릴리스하는 것도 쉬운 일이 아니었으며, 보통 많은 기업들의 릴리스 주기는 18개월 또는 24개월에 이르렀었다. 오늘날 데브옵스 팀의 경우에는 하루에도 여러 번 코드를 릴리스하고 있으며, 이는 대부분 자동화 덕분에 가능해졌다.


- 데브옵스 엔지니어가 따로 존재하는 조직과 따로 존재하지 않는 조직은 각각 어떤 장단점을 가지고 있을까요?.
* A = Devops를 사용 시에는 다음과 같은 이점이 있는데 장점은 다음과 같다.
    - 개발팀과 운영팀간의 의사소통 증가로 생산성 증대.
    - 한 곳에서 개발부터 검증, 배포까지 전체를 담당하게 되어 개발과 배포 속도가 빨라짐.
    - 구성원에게 개발 책임감과 코드의 소유권을 높여준다.
    - 개발 프로세스 간소화
반면 단점으로는
    - 다양한 팀이 모여 업무 역할이 변경되기 때문에 활성화되기 위해서는 충분한 시간이 필요함.
    - 코드를 자주 배포할 필요가 없다면 비용만 늘어남.
    - 포괄적인 자동화 도구가 필요함.


<h2>Quest</h2>

- 발급받은 AWS 계정에 접속해 봅니다.
- 본인의 루트 AWS 엑세스 키 ID와 비밀 엑세스 키를 생성하고, 본인의 로컬 머신에 저장해 놓습니다.
- 새로운 무언가를 생성하지는 않은 상태에서, 어떤 것들이 있는지 둘러봅니다.
- 과제 리뷰용 IAM 계정을 하나 만들어서 저에게 알려 주세요.
- 콘솔의 IAM 메뉴에 들어가서, 왼쪽의 엑세스 관리 -> 사용자에 들어가서 사용자 추가를 클릭합니다.
- 사용자 이름에 kcho@knowre.com을 입력하고, 
- 엑세스 유형에 프로그래밍 방식 엑세스와 AWS Management Console 액세스를 모두 클릭합니다.
- 자동 생성된 비밀번호와 비밀번호 재설정 필요를 체크합니다.
- 권한 설정에서 기존 정책 직접 연결을 선택한 뒤, 
- AdministratorAccess를 체크하고, 
- 하단의 다음:태그와 다음:검토를 계속해서 누른 뒤, 사용자를 만듭니다.
- 액세스 키 ID와 비밀 액세스 키, 비밀번호, 그리고 위의 안내에 써 있는 접속을 위한 
- https://[12자리숫자].signin.aws.amazon.com/console URL을 저에게(생략) 보내 주시면 됩니다!



<h2>Advanced</h2>

- SRE(Site Reliability Engineering)는 어떤 개념일까요?
* A = 사이트 신뢰성 엔지니어링(SRE)은 IT 운영에 대한 소프트웨어 엔지니어링 접근 방식입니다. SRE 팀은 소프트웨어를 툴로 활용하여 시스템을 관리하고, 문제를 해결하고, 운영 태스크를 자동화합니다.
SRE 팀은 기존에 운영 팀이 수동으로 하는 경우가 많았던 태스크를 받아 엔지니어 또는 운영 팀에 넘기고, 엔지니어 또는 운영 팀은 소프트웨어 및 자동화를 사용해 문제를 해결하고 프로덕션 시스템을 관리합니다. 
SRE는 확장 가능하고 신뢰성이 높은 소프트웨어 시스템을 생성할 때 유용한 방법입니다. 코드를 통해 대규모 시스템을 관리할 수 있으므로 수천 대에서 수십만 대에 이르는 머신을 관리하는 시스템 관리자에게 더 큰 확장성과 지속가능성을 제공합니다. 

- 미래의 데브옵스 직무는 어떻게 변화할까요? 여러 가지 미래를 상상해 봅시다!.
* A = https://www.itworld.co.kr/news/251626
