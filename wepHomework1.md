## web-blog project를 하며 알게된 용어 정리.
### webHomework1

1. ruby, gem, jekyll, bundler, msys, ridk, minGW, github pages, gcc, gnu, gpp, cli, gui, unix, linux, shell, kernel, user interface, local repository, remote repository, svn, git 용어 정리

>-> 아래에 정리.

2. 오늘 깃허브 블로그가 곧 올라 갈텐데 어떻게 다운로드 했는지 윈도우즈환경에서 정리

>-> [Project-TIL/make_GitHubBlog_with_githubpage 문서에 정리](https://github.com/SEOYEONGO/Project-TIL/blob/main/make_GitHubBlog_with_githubpage.md)


3. 도메인, 도메인 네임서버, 도메인 레코드들, 어떻게 도메인 연결했는지.

>-> [Project-TIL/make_GitHubBlog_with_githubpage 문서에 정리](https://github.com/SEOYEONGO/Project-TIL/blob/main/make_GitHubBlog_with_githubpage.md)


4. 깃허브 브랜치, 포크, 작업 환경에 대해 정리해보기

>-> [Project-TIL/about_GitHub 문서에 정리](https://github.com/SEOYEONGO/Project-TIL/blob/main/about_GitHub.md)


5. 블로그 사이트 정리, 포트폴리오 내용 정리

>-> https://seoyeongo.site 

---

### 1. ruby

스크립트 언어이자 순수 객체 지향 언어.


### 2. gem 

>레일즈가 프레임워크라고 한다면, 잼은 라이브러리다. 즉, 필요한 기능이 있을 때 추가해서 사용하면 됩니다. 

rubygem(Gem)이란 루비에서 지원하는 패키지 시스템으로 리눅스의 패키지 시스템인 yum apt emerge 같은 것으로 필요프로그램을 관리할 수 있는 프로그램입니다. 

Gem 또한 저런 시스템들과 마찬가지로 명령만 내리면 인터넷에서 자동으로 프로그램을 받아서 설치를 해줍니다. gem을 통해, 루비 프로그램과 라이브러리를 배포하는 표준 형식과 배포 방법을 제공하는것입니다.(node에서 사용하는 npm과 유사합니다.)
레일스 프로젝트를 생성하면 프로젝트 루트 디렉토리에 Gemfile이 자동으로 생성됩니다. Gemfile은 다양한 gem을 등록하는 파일로 텍스트 파일인 것입니다. 여기서 젬이란 다른 언어에서 흔히 접하게 되는 일종의 루비 라이브러리라고 생각하면 됩니다. 이미 많은  젬들이 공개(http://rubygems.org)되어 있기 때문에, 우리는 그저 필요한 젬을 다운받아 사용하기만 하면 됩니다.

쉽게 말해서!

루비 프로그래머는 gem을 이용해서 간단하게 원하는 프로그램을 설치할 수 있으며, 자신이 개발한 프로그램을 간단하게 배포할 수 있다.

따라서 레일스 프로젝트로 웹서비스를 제작할때 다른 gem들을 활용해 더 멋진 기능을 가진 웹사이트를 만들게 되는 것입니다!

>출처: https://ideveloper2.tistory.com/80


### 3. jekyll

Jekyll은 여러(특히 마크다운) 형태의 텍스트와 테마를 소스로 하여 정적 HTML 웹사이트를 제너레이트하는 툴이다. Ruby 스크립트로 만들어져 있으나, 블로그를 만드는 데에는 루비를 전혀 몰라도 된다. 워드프레스를 사용하여 블로그를 만드는 노력이면 워드프레스보다 훨씬 더 빠르고 보안에도 뛰어난 블로그를 깃허브에 무료로 만들 수 있고, 별도의 페이지를 만들기도 쉽다. 또한, HTML과 CSS에 대한 약간의 지식만 있으면 페이지는 물론 각 포스트마다 다른 레이아웃을 줄 수도 있다.

>출처: https://nolboo.kim/blog/2013/10/15/free-blog-with-github-jekyll/


### 4. bundler

번들러는 루비 애플리케이션을 위한 일관된 환경을 관리합니다. 번들러는 애플리케이션 코드와 실행하는데 필요한 루비젬을 추적하여 애플리케이션으로 하여금 항상 실행할 때 필요한 정확한 gem과 버전을 쓰도록 합니다. 


번들러를 사용하면 개발, 스테이징, 프로덕션 기기에서의 코드 공유가 쉬워집니다. 당연히 애플리케이션이나 gem을 공유하는 방법을 아시겠지만, GitHub에 붙여넣고 필요한 곳에서 클론하시면 됩니다. 번들러는 애플리케이션이 에러 없이 켜지고 실행하는데 필요한 의존성을 해결하는 일을 쉽게 합니다.

>출처: https://ruby-korea.github.io/bundler-site/v1.5/


### 5. msys & minGW

MinGW는 Linux의 GNU 컴파일러 관련 개발툴을 Windows에서 사용할 수 있도록 포팅한 프로젝트입니다.

MSYS는 MinGW에 포함되어 배포되는 별도 프로젝트인데, 쉽게 말해 Windows에서 실행되는 작은 Linux입니다.


MinGW = "Minimalist GNU for Windows"

MSYS = "Minimal SYStem", is a Bourne Shell command line interpreter system.

>출처: https://m.blog.naver.com/PostView.nhn?blogId=adapriest&logNo=220640049556&proxyReferer=https:%2F%2Fwww.google.com%2F


### 6. ridk

RubyInstaller-2.4 이상의 런타임 환경을 관리하는 도우미 도구입니다. cmd 및 powershell에서 사용할 수 있습니다.

>출처: https://smartbase.tistory.com/42
  
  
### 7. github pages

깃허브의 기능 중 하나. 저장소에 홈페이지 파일을 올린 뒤 저장소의 주소를 그대로 홈페이지 주소로 사용할 수 있는 기능이다. 이 기능을 사용하면 깃허브 저장소를 웹 서버처럼 활용할 수 있기 때문에 무료로 깃허브의 저장소를 블로그나 홈페이지 공간으로 사용할 수 있다. 
(Boostrap 또한 GitHub Pages를 사용해 만든 홈페이지이다.)

---

### 8. gcc

- GNU Compiler Collection

- 원래 gcc는 C만을 지원하였던 컴파일러라고 합니다, 이름 역시 "GNU C Compiler" 였다고 하는군요. 하지만 시간이 흐른 후에 Java, C++, 포트란, 에이다 C#, android 등등 여러 언어들을 컴파일 할 수 있게 되면서 현재의 이름도 변경되었다고 합니다.

>출처: https://splug.tistory.com/170


### 9. gnu   GNU/리눅스
 
 리눅스는 운영체제입니다. 운영체제는 여러가지 프로그램의 모음으로, 이 프로그램을 이용해 컴퓨터를 사용하고 다른 프로그램을 실행하기도 합니다.

운영체제의 가장 중요한 부분이 바로 커널입니다, GNU/리눅스 시스템에서 리눅스는 커널 부분을 말합니다. 시스템의 나머지 부분은 기타 프로그램으로 구성되며, GNU 프로젝트가 많은 부분을 개발했습니다. 리눅스 커널 그 자체만으로는 시스템을 구성할 수 없기 때문에, 우리는 흔히 리눅스라고 호칭하는 시스템을 GNU/리눅스라는 이름으로 사용합니다.

>출처: https://www.debian.org/releases/jessie/mips/ch01s02.html.ko


### 10. gpp

파일 확장자 GPP란 무엇입니까?

Serif은(는) Serif DrawPlus 소프트웨어 시리즈를 위해 Guitar Practiced Perfectly 2 Data File(GPP) 파일을 개발했습니다. 일반적으로 Guitar Practiced Perfectly 2 Data File 파일은 United States의 사용자 컴퓨터와 Windows 10 운영 체제를 실행하는 PC에서 발견됩니다. 이 사용자들의 대부분은 기본 인터넷 브라우저를 Google Chrome로 사용하기를 선택했습니다.

>출처: https://www.fileviewpro.com/ko/file-extension-gpp/


### 11. shell script

: 운영체제의 쉘 즉 bash, ksh, csh 등이 읽어 실행해주는 스크립트 언어


> 쉘 스크립트를 이해하려면 먼저 스크립트(Script)가 무엇인지 이해해야 한다. 스크립트란 일반적으로 인터프리트(interpret) 방식으로 동작하는 컴파일되지 않은 프로그램이라고 이해하면 된다. 즉 "프로그램의 한 라인을 읽어 해석하고 실행하는 과정을 반복하도록 만들어진 프로그래밍 언어로 작성된 컴파일되지 않은 파일에 저장된 프로그램"이라는 의미다. 조금 어려운가? 그렇다면 다음과 같이 이해하자.

> 텍스트 형식으로 저장되는 프로그램으로서 한줄씩 순차적으로 읽어 실행되도록 작성된 프로그램이다.

> 스크립트는 위의 정의(?)와 같다. 그렇다면 쉘 스크립트는 스크립트와 무엇이 다를까? 아마도 이런 말들을 들어보았을 것이다.
> 쉘 스크립트, 펄 스크립트, 자바 스크립트 등등등....

> 스크립트라는 단어 앞에 여러가지 수식어(?)가 붙는다. 이 수식어는 바로 스크립트를 읽어 실행해주는 인터프리트 엔진을 말한다고 이해하면 된다. 즉 쉘스크립트는 운영체제의 쉘 즉 bash, ksh, csh 등이 읽어 실행해주는 스크립트 언어이고 펄 스크립트는 perl 이라고하는 인터프리트 엔진이 읽어 실행해주는 스크립트 언어다. 그렇다면 자바 스크립트는 누가 읽어 실행해 주는 스크립트 언어일까? 그것은 바로 인터넷익스플러어와 같은 웹브라우저다. 물론 크롬 브라우저도 자바스크립트를 읽어 실행해준다.

> 각각의 스크립트 언어들은 문법이 모두 다르기 때문에 호환되지 않는다. 또한 실행파일을 만들때 작성되는 C언어와도 다르다. 

>출처: https://naltaengi.tistory.com/18


--- 

### 12. GUI

GUI(Graphic User Interface): 그래픽 기반 사용자 인터페이스. 

컴퓨터와 사람이 만나는 화면이 그랙픽 적으로 제공됨.

운영체제 바탕화면에 아이콘을 마우스로 더블클랙해서 프로그램을 실행하는 방식.


### 13. CLI 
CLI(Command Line Interface) 또는 CUI(Character User Interface): 명령줄 인터페이스. 

검은색 화면에 흰색 글자가 나오는 화면만 제공하는 운영체제.


### 14. user interface

사용자 인터페이스(영어: user interface, UI)는 사람(사용자)과 사물 또는 시스템, 특히 기계, 컴퓨터 프로그램 등 사이에서 의사소통을 할 수 있도록 일시적 또는 영구적인 접근을 목적으로 만들어진 물리적, 가상적 매개체를 뜻한다. 사용자 인터페이스는 사람들이 컴퓨터와 상호 작용하는 시스템이다. 사용자 인터페이스는 물리적인 하드웨어와 논리적인 소프트웨어 요소를 포함한다. 사용자 인터페이스는 크게 다음과 같은 수단을 사용한다.

- 입력: 사용자가 시스템을 조작할 수 있게 한다.
- 출력: 시스템이 사용자가 이용한 것에 대한 결과를 표시한다.
- 삭제: 시스템이 사용자가 잘못한것을 삭제한다.

+ interface
인터페이스는 inter(사이의)와 face의 합성어. 얼굴과 얼굴 사이라는 뜻.

인터페이스는 시스템과 시스템의 경계를 의미할 때 사용하기도 하고, 시스템과 사람, 장치와 소프트웨어간의 경계를 말할 때 사용한다.


### 15. Linux

-> [이 페이지의 9번 참조](##9. gnu   GNU/리눅스)


### 16. kernel

커널(kernel)은 운영체제의 핵심 소프트웨어. 운영체제의 커널이 CPU, RAM, 디스크, 네트워크 등의 하드웨어를 관리한다.
>커널은 특권모드(privileged mode)야.


### 17. shell 

셸(shell)은 사용자가 컴퓨터에 내린 명령을 번역해주고 커널에 이 명령을 전달하는 응용프로그램이다.

셸은 커널과 사용자가 대화할 수 있도록 도와주는 소프트웨어임.
>사용자가 명령을 내림 -> 셸(shell)과 응용프로그램이 커널(kernel)에게 명령을 번역 후 전달 -> 운영체제의 커널(kernel)이 하드웨어를 관리


---
### 18. local repository

로컬 저장소(Local Repository): 내 PC에 파일이 저장되는 개인 전용 저장소입니다.

>출처: https://backlog.com/git-tutorial/kr/intro/intro1_2.html


### 19. remote repository

원격 저장소(Remote Repository): 파일이 원격 저장소 전용 서버에서 관리되며 여러 사람이 함께 공유하기 위한 저장소입니다.

>출처: https://backlog.com/git-tutorial/kr/intro/intro1_2.html


---

### 20. svn

#### SVN 이란?(정의) SVN 사용 이유

SVN은 SubVersion의 줄임말로 형상관리/소스 관리 툴이다

SVN은 **여러명이서 작업하는 프로젝트의 경우 버전관리나 각자 만든 소스의 통합과 같은 문제를 해결하기 위해**, 장소를 만들어 그곳에 소스를 저장해 소스 중복이나 여러 문제를 해결하기 위한 Software이다.

>하나의 서버에서 소스를 쉽고 유용하게 관리할 수 있게 도와주는 툴


>프로젝트 소스는 SVN 서버의 Trunk라는 곳에 위치 -> 자신의 Local에 Trunk의 소스를 다운 받아(update) 수정 및 추가 후 다시 업로드(commit)하는 방식.

>자신만의 소스를 다른 개발자들과 떨어져서 작업하려면 Branch(원 소스의 나뭇가지)를 만들어 작업 후 자기자신만 접근하여 개발하며 

>완성되면 Merge 기능을 사용하여 Trunk와 소스를 합치면 된다.

>A가 자신이 수정한 소스나 폴더를 Commit하면 B는 해당 소스를 Update받으면 최신의 소스를 받아올 수 있다


**버전관리의 목적**

* 작업 이력 관리

* 문제 파악

* 예전 버전의 파일 복원

* 수정한 부분 검증

* 협업 지원

 

**버전관리 툴 용어**

- Repository: 프로젝트 파일 및 변경 정보가 저장되는 장소

- Import: 빈 Repository에 맨 처음 파일들을 채우는 것

- Export: 버전 관리 파일들을 뺀 순수 파일만 빼내는 것

- Checkout: 저장소에서 최신 버전의 소스코드를 최초로 받아오는 것 / Repository에서 프로젝트 관련 파일들을 받아온다

- Update: 로컬 저장소에 있는 파일들을 저장소의 최신 버전으로 받아 오기

- Commit: 로컬 저장소의 변경된 내용을 서버로 전송 / Checkout한 파일의 수정사항을 갱신

- Revert: 로컬 저장소의 내용을 이전 상태로 돌림

- Add: 버전관리 대상으로 파일 등록

- Trunk: 개발 소스를 commit 했을 때 개발 소스가 모이는 곳 / 프로젝트에서 가장 중심이 되는 디렉토리, 소스와 파일 포함

- Branch: trunk에서 분리/복사한 소스로 버전별 배포판을 만들거나 trunk와 별도로 운영환경을 위한 안정화된 소스 관리 목적으로 사용

- Tag: 특정 시점의 상태 보존 목적으로 사용 장기적으로 1.0, 1.1 등 버전 별로 소스 코드를 따로 저장. 특정 시점에서 프로젝트의 스냅샷을 찍어두는 것

>출처: https://na27.tistory.com/211 [na27]


### 21. git 용어 정리

-> Project-TIL/about_GitHub 문서에 정리. 





