## 네트워크 / 웹 / 실습

2. 웹

### 2번: 그래서 WEB이 뭐야?<br><br>

**웹**... 자 웹의 시초를 보면, 팀 버너스리께서 Word-Wide Web를 만드셨어. <br>
>팀 버너스리는, 영국의 컴퓨터 학자. www, URL, HTTP 등을 고안하여 웹을 탄생시킨 아버지로 유명하다.<br>
>월드 와이드 웹(World Wide Web, WWW, W3)은 인터넷에 연결된 컴퓨터를 이용해 사람들과 정보를 공유할 수 있는 거미줄(Web)처럼 얼기설기 엮인 공간을 뜻하는 용어다. <br> HTTP 프로토콜을 기반으로 HTML로 작성된 하이퍼텍스트 페이지를 웹 브라우저라는 특정한 프로그램으로 읽을 수 있게 하도록 구성되어 있다. WWW, W3, 또는 간단하게 웹(Web)이라고도 한다. <br> 
<br>

월드와이드웹은 인터넷 상에 연결된 온라인 상의 공간이지롱<br>

참고하기 아주 좋은 영상이 있쒈 : https://www.youtube.com/watch?v=A3aKQvLZpFA&feature=emb_rel_end    <br>


       웹(WEB)의 첫번째 특징: 한대의 컴퓨터에서 처리하지 않는다. 반드시 서버와 클라이언트가 존재한다! 
       클라이언트가 서버에게 requests를 보내고 / 서버는 클라이언트에게 responses를 보내고 ...그런 사이야 

--

### 웹서버는 또 뭔데? 

자...**웹브라우저**가 있다? 1. 웹브라우저로 처리할 데이터를 입력해.<br>
2. <u>**웹브라우저**에서</u> **웹서버 애플리케이션**에게 **데이터 처리 요청을 전송**하지.<br>
>웹 애플리케이션은 웹브라우저를 유저 인터페이스로 이용하는 애플리케이션이래. <br>
3. 웹서버가 [애플리케이션 서버/데이터베이스 서버]에 데이터 처리를 요청해. (애플리케이션 서버와 데이터베이스 서버가 연계해 요청받은 처리를 한다.)<br>
4. [애플리케이션 서버/데이터베이스 서버]가 힘을 합쳐 데이터 처리 결과를 [웹서버]에 돌려보낸다.<br>
5. [웹서버]는 [웹브라우저]에 데이터 처리 결과를 표시하는 웹페이지를 작성해서 돌려보낸다.<br>
6. 처리 결과 웹페이지를 [웹브라우저]로 표시한다.<br><br>

    1. 웹 서버(web server)<br>
    : 서버는 웹페이지, 사이트를 저장하는 컴퓨터<br>
    : 클리아언트가 웹페이지에 대한 접근을 요청한다면, 서버에서 웹 브라우저로 웹 페이지의 사본이 다운로드된다.<br><br>
    
    ![Web server](https://media.vlpt.us/images/ljina0218/post/9c2472db-7cdd-4337-8c78-b1741894d208/image.png)
    <br><br>
    2. WAS(Web Application Server)<br>
    : 웹 애플리케이션과 서버 환경을 만들어 동작시키는 기능을 제공하는 소프트웨어 프레임워크<br>
    : 인터넷 상에서 http를 통해 사용자 컴퓨터나 장치에 애플리케이션을 수행해 주는 미들웨어<br><br>

        1) 웹 서버 기능(정적 데이터 처리)
        : 웹 애플리케이션에서 정적 데이터 처리를 위해 지연되는 시간을 줄여 동적 데이터 처리 속도를 높일 수 있다.

        2) 웹 컨테이너 기능(동적 데이터 처리)
        서블릿 컨테이너 (java -> class)
        jsp 컨테이너 (jsp -> java(servlet))
        : url과 서블릿을 맵핑하여 실행하고, 서블릿의 생명주기를 관리한다.
        : reqeust 객체와 response 객체를 주입해준다.
     이것에 대한 출처 : https://velog.io/@ljina0218/Web-Application-Server
     
 이쯤 난 머리가 삥글삥글 돌기 시작해... 모르는 용어들이 많이 나오그등...<br><br><br>
 
 **서블릿에 대한 이해가 필요해**

 ---
 
 ## 웹 관련 용어 정리<br><br>
 
TCP/IP<br>  OK
HTTP<br>   OK 
DNS<br>   OK 
컴포넌트 파일  **이건 뭘까?_?**       

웹브라우저 : 인터넷 상에서 HTTP로 작성된 문서...를 웹에서 컨텐츠로 보여주는 응용프로그램이다!

3-4 handshake : 안녕~~~ 데이터 보낸다~~~~ 나 종료한다~~~~

*프록시 서버의 포트번호 : 22
*HTTP의 웰토운포트 : 80

<br><br>
---
## HTTP<br><br>
HTTP(Hyper Text Transfer Protocol): 하이퍼텍스트 문서를 전달하기 위한 규약<br>
<br><br>
---

* Brute-force : 무작위 대윕 알고리즘<br>
* 공격키. 개인키. <br>
* port forwarding -> phpmyadmin????<br>
* PHP, MySQL<br>
* 터미널 접속은 22번(?), 22-7777, 22-80번, 윈도우 원격 : 3036, remote protocol(?)<br><br>

--
* 웹서버는 스태틱합니당...<br>
* 웹어플리케이션은 동적...<br><br>
--<br>
* 자바의 장점은, 어느 환경에서든지 돌아간다는 것인데, 그것은 JVM(자바벌츄얼머신) 덕분입니다!_!<br>
* JVM의 svervlet은 DataBase랑 뭔갈 주고 받아.<br><br>
--<br>
* SELECT *From'user' WHERE id=='Alice'<br>
-> 이게 무엇이야..?<br><br>
--<br>
* 자세한 것은 3-2 고급 웹프로그래밍ㅇ에서 다룰 듯..<br>
* 클라이언트 사이드(프론트엔드) / 서버 사이드 (백엔드)<br><br>
--<br>
* 컴포넌트 파일은 무엇이져..?<br>
* DNS : 주소->IP, IP-> 주소.<br>
* HTTP 메소드 종류 : GET과 POST (두개는 특정 리스크(?) 요청), PUT (콘텐츠 저장), Delete(리소스 삭제)<br>
* HTML과 HTTP<br><br>
--<br>

* 뭔가 요청이 들어오면, 프록시 서버를 거쳐서, 컨텐츠를 동적 생성한 후 그것을 정적으로 뿌려줘 (웹서버 어플리케이션)<br>
* 웹서버 : HTTP 요청을 받아서 동적으로 컨텐츠를 생성한다! <br><br>

* 비트나미가 뭐에영? 희희

**


---
## 클라우드<br><br>

서버는 왜 비싼가... 온도감지도 해줘야 해, 화재가 일어나면 그즉시 산소차단 분말가루(?)를 서버 기계에 촥 뿌려야 해... 관리가 힘들어!
그래서 서버관리는 관리자에게 맡기는 경우가 대다수.<br>

L<br>
A  Apache<br>
M  MySQL<br>
P  PHP<br>

그렇다..서버 운용과 관리에는 시간과 비용이 들어가니 필요한 자원을 가져다 쓰자는 말이 나왓어! 관리자한테서 우리는 필요한 것만 가져다 쓸게! 라고 하는 거지!_!
* 그것이 클라우드 서비스얌>.<
* 데이터 서비스, BTC
* 1등은 AWS이고 2등은 Google cloud platform Microsoft Azure, 3등은 IBM Clould
* 사실 AWS 서비스가 사내에서 쓰려고 했는데 너무 좋아서 BTB 서비스로 풀엇는데 반응이 조아써...<br><br>

1. IaaS : Infra structure as a service -> 예) AES의 EC2, Jclould
2. PaaS : Platfrom as a service -> 예) Deep Racer, RoboMaker, Aleax, 구름아이디(?)
3. SaaS : Software as a service

* 카톡도 AWS 기반의 서비스엿댕.
* code deploy 기능..아마 SaaS(?)


---
## 실습<br><br>

실습1 : AWS EC2 서버 만들기<br><br>

* 인스턴스 유형...C는 cpu power, i?, t? 코어 갯수..?
* gpu 머슨은 좀 비싸..하루애 10만원?
* 스팟인스턴스는...다른 유저의 남는 공간을 시간 단위로 빌려오는 것이야.
* Clouldwatch는... 모니터링을 해준다?
* 보안그룹은...외부에서 나한테 접근하려면 어떻게 해야하는지 설정해야 하는 것인가(?)
* 개인키/공격키
* CA : 인증서, Certification Auzthorization
* AWS Educate Starter Account는... 요금 오버되는 것을 막아요.. 1시간에 100원? 
* AWS의 제품군이 굉장히 많아요
* Amazon Elastic Clould 
* 서버용 CPU가 따로있어.
* 이더넷은 컴퓨터를 연결하는 체계야 (TCP/IP)
* 온디맨드가 머더라? 아아 사용자의 요구만큼만 사용하는 것이얌
* AMI(?)






--

AMP??<br>

실2 : AMP을 설치해보자<br><br>

Apache vs Nginx<br>
Node.js<br>
Node.js Express<br>


 
