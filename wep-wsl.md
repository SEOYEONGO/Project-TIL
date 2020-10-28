## wep-class (10.28)
### 목표: wsl을 설치해보자.


우선, wsl은 무엇일까?

> Linux용 Windows 하위 시스템이란?

Linux용 Windows 하위 시스템을 사용하면 개발자가 기존 가상 머신의 오버헤드 또는 듀얼 부팅 설정 없이 대부분의 명령줄 도구, 유틸리티 및 애플리케이션을 비롯한 
GNU/Linux 환경을 수정하지 않고 Windows에서 직접 실행할 수 있습니다.

| - 다음을 수행할 수 있습니다.
+  Microsoft Store에서 즐겨찾는 GNU/Linux 배포를 선택합니다.
+  grep, sed, awk 또는 다른 ELF-64 이진 파일과 같은 일반적인 명령줄 도구를 실행합니다.
+  다음을 포함하여 Bash 셸 스크립트 및 GNU/Linux 명령줄 애플리케이션을 실행합니다.
  *  도구: vim, emacs, tmux
  *  언어: NodeJS, Javascript, Python, Ruby, C/C++, C# 및 F#, Rust, Go 등
  *  서비스: SSHD, MySQL, Apache, lighttpd, MongoDB, PostgreSQL.
+  자체 GNU/Linux 배포 패키지 관리자를 사용하여 추가 소프트웨어를 설치합니다.
+  Unix와 같은 명령줄 셸을 사용하여 Windows 애플리케이션을 호출합니다.
+  Windows에서 GNU/Linux 애플리케이션을 호출합니다.

출처 : https://docs.microsoft.com/ko-kr/windows/wsl/about

| WSL1과 WSL2 비교
https://docs.microsoft.com/ko-kr/windows/wsl/compare-versions

리눅스는 init()으로..
bootloader
-> 윈도우 리누슥?
운영체제 2개 실행시킬 수가 잇어요

---

+ 부팅과 부트로더
> bootloader과 bootstrap

윈도우 OS, 맥 OS,리눅스 OS 모두 동등하게 512바이트 크기의 작은 코드에서 시작한다. 512바이트의 작은 코드는 '부트로더(Boot Loader)라고 불리며, OS의 나머지 코드를 메모리에 복사해 실행 시킨다.


##### 부팅과 BIOS

### 부팅

PC가 켜진 후에 OS가 실행되기 전까지 수행되는 일련의 작업 과정, 부팅 과정에서 수행하는 작업에는 프로세서 초기화(멀티코어 관련 처리 포함), 메모리와 외부 디바이스 검사 및 초기화, 부트로더를 메모리에 복사하고 OS를 시작하는 과정 등이 포함된다.

### BIOS

 PC 환경에서는 부팅 과정중 하드웨어와 관련된 작업을 BIOS(Basic Input/Output System)가 담당하며, BIOS에서 수행하는 각종 테스트나 초기화를 'POST(Power On Self Test)'라 부른다.

BIOS는 메인보드에 포함된 펌웨어의 일종으로, 이름 그대로 입출력을 담당하는 작은 프로그램이다. 보통 PC메인 보드에 롬(ROM)이나 플래시 메모리로 존재하며, 전원이 켜짐과 동시에 프로세서가 가장 먼저 실행하는 코드이다.

~>또한 BIOS는 부팅 옵션 설정이나 시스템 전반적인 설정 값을 관리하는 역할도 겸하고 있으며, 설정 값으로 시스템을 초기화 하여 OS를 실행할 수 있는 환경을 만든다.

~>BIOS에서 제공하는 기능은 '인터럽트'를 통해 사용할 수 있으며, MS-Dos 같은 과거의 16비트 OS는 BIOS 기능에 많이 의존하였다. 

출처: https://symnoisy.tistory.com/entry/4부팅과-부트로더1이론 [symnoisy]


---

+ Rom과 Ram

메모리(Memory)는 데이터를 기록하거나 읽기 위한 저장공간이며, 크게 램(RAM : Random Access Memory)과  롬(ROM : Read Only Memory)으로 분류할 수 있습니다.  



램(RAM)은 전원이 끊어지면 기억되어있는 데이터들이 소멸되기 때문에 휘발성 메모리(Volatile Memory)라 표현합니다.

데이터를 읽는 속도와 기록하는 속도가 같으며, 컴퓨터의 주기억장치, 응용 프로그램 로딩, 데이터 일시 저장등과 같은 곳에 사용됩니다.



- SRAM (Static RAM)

정적램이라 표현하며, DRAM에 비해 용량은 적으나 5배 정도 속도가 빠르고, 가격이 비쌉니다. 



- DRAM (Dynamic RAM)

동적램이라 표현하며, IC집적도가 SRAM에 비해 높기 때문에 용량은 크지만 속도가 느리며, 비교적 가격이 저렴합니다.

저장공간마다 캐패시터(전기 저장)를 사용하기 때문에 전원이 연결된 상태로 시간이 흘러 캐패시터에 있는 전기가 누설될 

경우 데이터가 유실될 수 있습니다.



- PSRAM (Pseudo SRAM)

내부에 전하 충전회로를 내장하여 DRAM의 단점을 보완한 RAM입니다. 주기적으로 전하충전이 되기 때문에 데이터 유실을

막을 수 있으며, SRAM처럼 사용할 수 있습니다.

 

- SDRAM (Synchronous DRAM)

100MHz 이상의 버스 속도를 유지하는 기능을 개발하여 내장한 DRAM의 일종입니다. 시스템의 클럭속도(보통은 CPU의 속도)와 동기화하여 동작할 수 있기때문에 CPU가 동작할 때 DRAM도 함께 움직여 CPU가 수행할 수 있는 명령어를 증가시킴으로써 최고의 효율로 작동시킬 수 있습니다.



- DDR SDRAM (Double Data Rate SDRAM)

SDRAM보다 처리속도가 2배 빠른 RAM입니다. 시스템버스 클럭의 Rising edge와 Falling edge를 동작시켜 같은 속도, 같은 시간내에 2배의 데이터를 보낼 수 있습니다. 즉, 100MHz로 작동하는 DDR SDRAM은 200MHz로 작동하는 SDRAM과 같습니다.





 





롬(ROM)은 전원이 끊어져도 기록된 데이터들이 소멸되지 않는 비휘발성 메모리(Non-Volatile Memory)입니다.

즉, ROM에 데이터를 (반영구적으로) 저장한 후 이를 지속적으로 사용하게 됩니다. 컴퓨터의 바이오스롬도 이에 속합니다.

일반적인 롬은 데이터를 한번 저장하면 지울 수 없이 계속 사용해야하지만, PROM(1번 다시 쓰기가능), EPROM(무한), 

EEPROM(무한)은 특수한 방법을 통해 데이터를 삭제한 후 데이터를 다시 기록할 수 있습니다.



- MASK ROM

가장 기본적인 ROM으로써, 제조사가 ROM 제조시에 데이터를 미리 저장해둡니다. 저장된 데이터는 변경할 수 없습니다.



- PROM (Programmable ROM)

저장된 데이터를 지우고 1회 수정할 수 있는 ROM입니다. 모든 저장공간에 퓨즈가 연결되어있으며, 데이터를 기록할 경우

퓨즈가 끊겨 데이터 수정이 불가능해집니다.



- EPROM (Erasable PROM)

메모리에 저장된 데이터를 지우고, 다시 저장할 수 있는 ROM입니다. 데이터를 지우는 방식에 따라 UVEPROM과 EEPROM으로 분류합니다.



- UVEPROM (Ultra-Violet EPROM)

자외선을 사용하여 저장된 데이터를 지울 수 있는 ROM입니다.



- EEPROM (Electrically Erasable PROM)

전기적인 기능을 통해 저장된 데이터를 지울 수 있는 ROM입니다. 정격전압보다 높은 고전앞을 통해 데이터를 지울 수 

있으며, 1바이트씩 데이터를 지우기 때문에 속도가 매우 느린편입니다. 





 





램(RAM)과 롬(ROM)의 차이점을 간단하게 나타내보자면.. 다음과 같습니다.

램(RAM)

읽기 쓰기 가능. 빠르다. 휘발성 메모리

롬(ROM)

읽기만 가능. 비교적 느리다. 비 휘발성 메모리

출처 : http://www.makeshare.org/bbs/board.php?bo_table=Parts&wr_id=24


---

+ virtual machine과 virtual Box

가상 머신(Virtual Machine, VM)은 단순하게 컴퓨터 기능을 가상으로 흉내내는 에뮬레이터 기능을 하는 프로그램이다.

버추얼박스의 최대 장점은 운영체제를 1개 이상 동시에 실행할 수 있는 것이다. 웹사이트를 윈도우에서 테스트하고 리눅스에서 실제 운영하는 것이 가능하다. 또한, 버추얼박스는 사용하기 쉽다. 설치 마법사를 이용해 새 VM을 설정할 수 있고 추천하는 설정도 제공한다. 반면 단점은 성능이다. 많은 사용자가 속도에 대해 불만을 제기하고 있다.

원문보기: http://www.ciokorea.com/news/36043#csidxf20a968915c70609d037fbb494cfad9 


Physical machine 위에 os(hos). 그 위에 superviser (가상머신을 관리해줘), 그위에 VM

하나의 supervisor위에 os세개 
가상 컨테이너. 컨테이너를 이미지로 만들 수가 잇어

리눅스용 윈도우 하위 시스템이란?

서로 앙숙이었는데 힘을 합쳣어!


windows subsystem linux
| 개발도구
| 명령어 해석기 (인터프리터) 
| 컴파일
듀얼뷰팅, 가상머신을 쓰기 위해 wsl


wsl 1 
kernel / bash / 뭐뭐

윈도우즈라는 커다란 소프웨어 안에서 
리눅스를 실행시킬 수 있는 자그마한 가상공간을 만들엇어 
virtual space
kernel

안드로이드는 안돼... 또 뭐도 잘안돼...

etc . home . 
c:\\
절대경로로 윈도우즈파일에 접근해
wsl 

wsl 을 깔거야 
듀얼 ios를 하고 

근데 오
도커… 

shell : (default) bash

cd ~

clear

alias 은 별명이야.


bashrc

bashrc는 bash에서 작업할 때마다 수행되는 파일.
환경변수 개념.
별칠(alias)과 bash가 수행될 때 실행되는 함수를 제어하는 지역적인 시스템 설정과 관련된 파일.


맥에서는 zsh가 기본이야. bash위에 zsh을 올려서. 이걸 쓰는 이유는 커스터마이징 쉬워..

---

프로그램과 프로세스 의 차이는…
프로그램 실행 중이다 => 프로세스.

---

-128 ~ 127

아스키코드는 0부터 255까지 표현 할 수 잇어

빅엔디안과 리틀엔디안.  -> 공부해두는 게 좋아.

유니코드는 한글을 지원해.

Naver의 D2Coding 

power line font -> 유니ㅣ코드를 지원해주는 폰트..



zshell을 깔아볼거야.


sudo apt install zsh

패키지 관리자. (package manger)

-> 리눅스에서는 apt -> mirror server
-> 윈도우에서 써본 것은 gem, yaum, npm
nano는 특정한 편집기가 필요없는 편집기

sudo vim etc/apt/s



리눅스 

	1. command mode
	2. line mode
	3. insert mode
a,i,o,O(그 다음줄), A(맨 첫번째에서 시작)

dd,  G   gg 

w q (쓰고 나가라)
q! (나가라)


indent space (들여쓰기)
spacebar
set nu  ->  source .vimrc


유닉스 시스템프로그래밍

---

gdb는 디버깅 툴이야.

gcc는 그누 컴파일러를 모아둔 것.

그누는 운영체제. 그누는 유닉스가 아냐. 리눅스야.

vim 편집기 재밋어

참고 : https://github.com/bonomoon/.vimrc/blob/master/.vimrc

vim은 단축기의 조합이 중요해.

여러가지가 있는데, dd, g, gg, yyy ppppp(복붙)

---

sudo는 superviser do인데, 관리자모드처럼 행동할 수 있게 해줘.

nano는 메모장 편집기.

Esc 누르면 command 모드

: 누르면 Line 모드

:i 누르면 Insert 모드

---

C언어 컴파일러 과정에 대해서 ...

https://gracefulprograming.tistory.com/16


커널은 관리자야. 슈퍼퐈월

int main (int argc, char **argv)
에서 argc는 argc = arguments count로 main 함수에 전달된 인자의 개수를 의미하며,

argv는 프로그램으로 전달된 실제 인수의 값이다. 이 값은 명령프롬프트창에서 문자를 치건 숫자를치건 무조건 문자열로 넘겨진다.
argv는 이중 포인터로서 문자열 배열을 가리키는 포인터 이다.
argv[0] 은 파일의 절대경로를 넘겨받고, 1부터 넘겨받는 인수가 저장된다.

char **argv과 char *argv[]는 동일한 표현이다.

++) env
운영체제의 환경변수를 넘겨받는다.
---

%s/archive.ubuntu.com/mirror.kakao.com.g
는 외국 서버(?)를 카카오 서버로 바꿔서 연결해주기 위한 것.

그래서 마지막에 mirror하고 sudo apt install gcc 깔고
sudo apt install gcc a.c (?) 했는데 아마 
한글 폰트가 깨지는 오류가 났다지??

---

오늘 배운 것을 정리해보자.

1. WSL 2 (쓰는 이유, 원리, 구조, 세팅)
2. Ubuntu 설치
3. vim 연습, .vimrc(빔 설정 파일)
4. mirror server 변경 => (update && upgrade)
5. gcc
6. 시스템 ~~~ (?)

---

그래서 다음 과제는...
1. Theme custom
2. pawerline font
3. vs code 기본 터미널을 ubuntu로 실행
참고 : https://medium.com/harrythegreat/oh-my-zsh-iterm2%EB%A1%9C-%ED%84%B0%EB%AF%B8%EB%84%90%EC%9D%84-%EB%8D%94-%EA%B0%95%EB%A0%A5%ED%95%98%EA%B2%8C-a105f2c01bec
