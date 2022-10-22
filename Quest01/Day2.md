# Quest 01. 리눅스와 친해지기

## Introduction
### 이번 퀘스트를 통해 리눅스의 기본적인 구조와 기능에 대해 공부할 수 있습니다.


# Topics
## 리눅스의 기본 커맨드
- cd, 
- pwd, 
- ls, 
- cp, 
- mv, 
- mkdir, 
- rm, 
- touch, 
- ln, 
- echo, 
- cat, 
- tail, 
- find, 
- ps, 
- kill, 
- grep, 
- wc, 
- df, 
- du
- 파이프(|) 문자


## 리눅스의 기본적인 디렉토리 구성
- /bin : binary의 약자로 실행파일 모음. 일반적으로 사용하는 mv, cat등 명령어 프로그램들이 있음

- /usr/bin : /bin과 유사한 역할을 한다. 콘솔에서 확장된 프로그램이 들어간다.
/bin과의 가장 큰 차이점은 general-system-wide 범위에서 사용가능하다는 점이다. 이에 속하는 바이너리 파일로는 sudo 명령어, vi 명령어 등이 위치한다.

- /boot : 부팅과 관련된 파일들이 모여있음 

- /dev : device의 약자로 물리적인 장치들이 파일화 되어 있다.

- /etc : 각종 환경 설정 파일들이 모여 있음

- /home : 개인사용자들 디렉토리

- /lib : 각종 라이브러리 저장 디렉토리

- /mnt : CD-ROM, 네트워크 파일 시스템 등을 마운트 할때 사용되는 디렉토리

- /proc : 현재 실행되고 있는 프로세스들이 파일화 되어서 저장되는 디렉토리

- /root : root계정의 홈 디렉토리

- /sbin : System-binary의 약자로, 주로 시스템 관리자가 쓰는 시스템 관련 명령어 프로그램들이 모여있다. /bin과 같은 역할을 한다. 그러나 실행하기 위해서는 root 권한이 필요하다.

- /usr/sbin : /usr/bin과 유사한 역할을 한다. 그러나 실행하기 위해서는 root 권한이 필요하다.

- /tmp : 임시 저장 디렉토리. 일반적으로 모든 사용자들에게 열려 있음

- /usr : 주로 새로 설치되는 프로그램들이 저장됨. '명령어' 보다 '프로그램'이라 부르는것이 더 익숙한 것들이 저장된다. 윈도우의 Program Files같은 폴더

- /var : 시스템 로그, 스풀링 파일 들이 저장된다. 메일 서버로 운영될 경우 메일이 여기 저장된다



## 쉘과 환경변수와 퍼미션
- sh : 쉘(Shell)은 받은 명령(Command)을 보낼 수있는 사용자 인터페이스로 작동하는 프로그램입니다 . 그런 다음 커널(Kernel)은 명령을 해석하고 CPU 및 기타 컴퓨터 하드웨어에 특정 작업을 수행하는 방법을 알려줍니다

- bash :  Bourne Again Shell의 줄임말로 스티븐 본이 개발한 최초 유닉스 프로그램인 sh의 확장판이다. 쉘을 포함한 모든 유닉스 쉘, 공통 기본 기능이 포함되어 파이프라인, here document, 명령 치환, 변수, 제어 구조 및 와일드 카드등의 기능이 있고, 사용자 계정에 대한 가장 일반적인 기본 셸입니다.
- zsh : 대화 형 사용을 위해 설계되었습니다. z셸의 일부 기능에는 맞춤법 검사, 단일 버퍼에서 여러 줄 명령 편집, 개선된 변수 및 배열 처리, 사용자 지정, 프로그래밍 가능한 명령줄 완성 및 테마가 있는 프롬프트가 포함됩니다. (bash와 유사하나 zsh이 부가적인 기능을 포함해 좀 더 편리하다고 평가됨)

- csh : C Shell이다. 빌조이(Bill Joy)가 캘리포니아 버클리 대학에서 만들었고, 주요 의도는 C 언어와 유사한 구문으로 쉘을 만드는 것이었습니다. 따라서 제어 구조 및 표현 문법과 같은 항목이 포함되었습니다. 다른 기능에는 기록 및 편집 메커니즘, aliases(별칭?), 디렉터리 스택, 물결표 표기법, cdpath, 작업 제어 및 경로 해싱이 포함됩니다.

- tcsh : tcshC 쉘과 호환되도록 개발되었고, t in tcsh은 운영체제인 TENEX에서 따왔습니다. tcshcsh명령줄 완성, 명령줄 편집 및 기타 기능과 같은 확장 기능에 매우 가깝습니다 . Mac OS X tcsh는 기본적으로 제공되지만 버전 10.3에서 bash로 전환되었습니다.

- .bash_profile : 

- .bashrc : 

- .zshrc

- env :  env는 bash에서 환경 변수를 조회하거나 등록하는 명령어다. 그냥 env만 붙이면 시스템에 등록된 환경변수들이 출력된다. 환경변수나 쉘 변수는 $를 붙여서 조회할수있다.
    ```$ env [변수명] ```

- set : set는 쉘 변수 관련 명령어로 set을 통해 쉘변수를 만들수도 있고 변수명에 값을 할당해 주는 방식으로 생성할 수도 있다.
    ``` $ set [변수명]=[값]```

- unset : unset은 쉘변수를 해제하기 위해서 사용한다 (환경변수에도 적용할 수 있다.)
    ```$ unset [변수명]```

- export: ​export를 사용하면 쉘 변수를 환경 변수로 만들 수도 있다
    ```$export [환경변수명]```

- chmod : chmod는 파일의 권한을 바꾸어 주는 명령어이다. 
    ```$ chmod [변경할 권한 대상] +[부여할 권한] -[없앨 권한] ...[대상 파일명]```

- chown : chown은 파일이나 디렉토리를 소유하고 있는 유저를 변경하는 명령어이다.
    ```$ chown [유저]:[그룹] [파일명/ 경로]```

- chgrp : chrgp 명령어는 unix계열 운영 체제의 일반 사용자들이 파일 시스템 오브젝트에 연결된 그룹을 변경하는 명령어이다. 파일 시스템 오브젝트에는 3가지 집합의 접근 권한이 있는데 그 중 하나가 소유자를 위한 것이고, 다른 하나가 그룹을 위한 것이며, 나머지 하나가 기타 사용자를 위한 것이다.
    ```$ chrgp [옵션] [그룹]```
    
- sudo : 유저가 소유권을 가지지 못한 파일을 실행할 경우 루트권한이 필요하다 이때, 루트 권한을 얻어오기 위해 사용하는 명령어가 sudo명령어로 root권한으로 명령을 할수 있도록 해주는 명령어이다. sudo를 사용할 경우 소유권을 가지지 못한 파일의 접근 권한도 변경하는것이 가능하다.

- setuid : 

- Sticky bit : 

### 운영체제의 기초
- 프로세스와 쓰레드
- 파일 시스템


### 리눅스의 배포판
- Ubuntu, Debian, Redhat Enterprise, CentOS,  Gentoo, Amazon Linux
- 패키지 시스템: apt(.deb), yum(.rpm)


### vi
- i, 
- w, 
- q, 
- u, 
- d, 
- p

## Resources

- The Linux command line for beginners
https://ubuntu.com/tutorials/command-line-for-beginners#1-overview

- The Linux Directory Structure, Explained
https://www.howtogeek.com/117435/htg-explains-the-linux-directory-structure-explained/

- Unix / Linux - What is Shells?
https://www.tutorialspoint.com/unix/unix-what-is-shell.htm

- zsh
https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH

- About systemd
https://www.infoworld.com/article/2832405/what-is-systemd-and-why-does-it-matter-to-linux-users.html

- About linux distributions
https://thebloggingpot.com/2018/05/23/different-linux-distributions-explained/

- RPM and YUM package management
https://developer.ibm.com/technologies/linux/tutorials/l-lpic1-102-5/

- File editing with vi
https://developer.ibm.com/technologies/linux/tutorials/l-lpic1-103-8/


# Checklist
- 리눅스의 파이프 문자는 어떤 역할을 하나요?
- 리눅스의 셸은 어떤 역할을 하나요? bash와 zsh는 어떻게 다른가요?
- 리눅스의 권한 체계는 어떻게 이루어져 있나요?
- 프로세스와 쓰레드는 무엇인가요?
- 현재 실행되고 있는 프로세스들 중 PID가 1인 프로세스는 어떤 역할을 할까요? init과 systemd는 무엇이고 어떻게 다른가요?
- 파일시스템이란 무엇일까요? 어떤 것이 있을까요? 지금 다루는 운영체제는 어떤 파일시스템을 쓰고 있나요?
- 리눅스의 배포판이란 무엇일까요? 여러 가지 배포판들은 어떻게 생겨났을까요?
- 리눅스의 패키지 시스템이란 무엇일까요? 이러한 시스템이 생긴 이유는 무엇일까요?  deb과 rpm은 어떤 차이가 있을까요? RPM이 있는데 yum과 같은 시스템이 나온 이유는 무엇일까요?
- vi는 어떤 에디터인가요? vi와 vim은 어떻게 다를까요? vi는 왜 모든 리눅스의 기본 에디터가 되었을까요?


# Quest
- 인스턴스 생성
- t3.nano 등급으로 EC2 인스턴스를 생성해 봅시다! Amazon Linux 2, Ubuntu 두 가지를 각각 생성해 봅니다.
- EC2 생성 과정에서 .pem 파일이 하나 생기는데, 이는 저에게 슬랙을 통해 공유해 주시면 됩니다.
- 세 배포판은 어떻게 다른가요?

# 리눅스 연습
- Amazon Linux 2 인스턴스에서 위의 Topics의 기본 커맨드를 연습해 봅니다.
- 리눅스의 기본 디렉토리들에 어떤 정보들이 있는지 둘러 봅니다.
- zsh를 설치하고 .zshrc 파일을 포함해 여러 가지 설정을 해 봅니다.
- Topics의 환경변수나 퍼미션 관련 커맨드를 연습해 봅니다.
- 현재 실행되고 있는 프로세스들과 마운트 된 파일시스템들을 확인해 봅니다.
- vi를 열어 여러 가지 기본 명령과 간단한 편집 방법을 연습해 봅니다.
- 생성한 인스턴스 중 Ubuntu는 완전히 종료(Terminate)하고, Amazon Linux 2는 일단 꺼둡니다.

# Advanced
- 리눅스 외의 POSIX 호환 운영체제에는 어떤 것들이 있을까요? 그러한 운영체제들은 어떤 용도로 쓰일까요?
- 윈도우를 제외하고, 최근에 발표된 운영체제들 중 POSIX에 호환되지 않는 운영체제도 있을까요?