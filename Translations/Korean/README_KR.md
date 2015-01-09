백앤드 개발자 면접 문제 은행
======================================

@Version 1.0

이 저장소에는 백앤드 개발자 면접에 나왔던 문제들이 있습니다.
여기에 있는 모든 문제들은 푸는 것(꽤 많은 시간이 걸릴 것입니다)보다는
여기서 몇 가지 질문을 골라 자신의 실력을  평가해보는 것이 좋을 것입니다.

##한국어 번역

@DevSusu

##<a name="toc">목차</a>
* [기여자](#contributors)
* [일반 질문](#general)
* [디자인 패턴 관련 질문](#dpspecific)
	* [MVC](#mvcspecific)
	* [MVVM](#mvvmspecific)
	* [리파지토리](#repospecific)
	* [의존성 주입](#dispecific)
	* [방문자](#vspecific)
* [PHP 코드 예제](#phpcodeexamples)
* [PHP 관련 질문](#phpspecific)
* [데이터베이스 관련 질문](#databasespecific)
* [객체 관계 매핑ORM 관련 질문](#ormspecific)
	* [원칙](#doctrine)
* [HTTP 관련 질문](#httpspecific)
* [운영체제 관련 질문](#osespecific)
* [웹 서비스 관련 질문](#webservicesespecific)
	* [대표적인 서버 응답 코드](#csrcspecific)
* [네트워크 관련 질문](#networkspecific)

###<a name="contributors">기여자</a>

* [@travisvandame](http://twitter.com/travisvandame)
* [@jmurowaniecki](http://twitter.com/jmurowaniecki)
* [@emanuelsaringan](http://lambdageek.com)

**[[⬆]](#toc) 목차로 되돌아가기**

###<a name="general">일반 질문</a>

* 당신은 이번주/어제에 무엇을 배웠습니까?
* 코딩을 하는데에 당신을 자극하는것이 무엇입니까?
* 사용해 본 경험이 있는 버전관리 시스템엔 어떤 것들이 있습니까(깃, SVN 등)?
* 당신이 선호하는 개발 환경은 어떤 것입니까? (운영체제, 편집기, 브라우저, 개발툴 등)
* PHP 테스팅을 어떻게 시작하십니까?
* 당신이 쓴 라이브러리/프레임워크의 소스 코드를 살펴본 적이 있습니까?
* 당신의 코드를 어떻게 관리합니까?
* 당신의 코드를 어떻게 최적화합니까?
* 만약에 당신이 단 하나의 기술을 완벽히 익힐 수 있다면 무엇을 익히겠습니까?
* 표준과 표준체의 중요성에 대해서 설명하십시오.
* MVC와 HMVC에 대해서 설명하고 둘의 차이점, 목표와 장점에 대해 설명하시오.
* 애자일 방법론에 대해서 배웠거나 알고있는 사실에 대해 말하시오.
* 혼자 일하는 것을 즐기십니까, 팀으로 일하는 것을 즐기십니까?
* 당신이 프로젝트 진행 중 마주했던 가장 큰 문제가 무엇이었으며, 그것을 어떻게 해결하였습니까?
* 오픈소스 커뮤니티에 어떻게 기여하십니까? (깃허브, Bitbucket, IRC, 포럼)

**[[⬆]](#toc) 목차로 되돌아가기**

###<a name="dpspecific">디자인 패턴 관련 질문</a>

* <a name="mvcspecific">MVC</a>
* <a name="mvvmspecific">MVVM</a>
* <a name="repospecific">레파지토리 패턴</a>
* <a name="dispecific">의존성 주입</a>
* <a name="vspecific">방문자 패턴</a>
    * 이 패턴에 들어가는 클래스와 객체들은 무엇이 있는가? **답변: Visitor, ConcreteVisitor, Element, ConcreteElement, ObjectStructure**

**[[⬆]](#toc) 목차로 되돌아가기**

###<a name="phpcodeexamples">PHP 코드 예제:</a>

```php
floor(3.14)
```
질문: 위 코드에 의해 반환되는 값은 무엇인가? **답: 3**

```php
echo join("", array_reverse(str_split("i'm a lasagna hog")));
```
질문: 위 코드에 의해 반환되는 값은 무엇인가? **답: "goh angasal a m'i"**

```PHP
$array = array();

array_push($array, 1);
array_push($array, 2);
```
질문: `count($array)` 의 값은 무엇인가? **답: 2**

```PHP
$foo = "Hello";

function alert_a() {
	global $foo;

	$bar = " World";

	echo ($foo . $bar);
}

function alert_b() {
	$bar = " World";

	echo ($foo . $bar);
}

alert_a();
alert_b();
```
질문: 위 두개 alert의 결과는 무엇인가? **답: alert_a() = Hello World, alert_b() = E_NOTICE : type 8 -- Undefined variable: foo -- at line 15 World**

**[[⬆]](#toc) 목차로 되돌아가기**

###<a name="phpspecific">PHP 관련 질문</a>

* 콜백을 쓰는 두 가지 좋은 실례를 설명하시오.

**[[⬆]](#toc) 목차로 되돌아가기**

###<a name="databasespecific">데이터베이스 관련 질문</a>

* 일반 SQL
	* 뷰와 테이블의 차이점이 무엇인가?
	* HAVING 문이 하는 일이 무엇인가?
	* 인덱싱할 열을 어떻게 선택하는가?
* General SQL
	* What is the difference between a View and a Table?
	* What does the HAVING clause do?
	* How do you choose a column to be indexed?
* MySQL 관련 질문
	* 당신은 어떻게 커맨드 라인을 사용하여 mysqldump로부터 데이터를 백업하고 복구하겠는가?
	* 어떤 상황에서 SQL_CACHE와 S_NO_CACHE를 쿼리에서 쓸 것인가?
	* 질문: 캐시를 불활성화하는 5개의 함수를 설명하고 왜 그런지도 설명하라.
		**답변: BENCHMARK(), CONNECTION_ID(), CONVERT_TZ(), CURDATE(), CURRENT_DATE(), CURRENT_TIME(), CURRENT_TIMESTAMP(), CURTIME(), DATABASE(), ENCRYPT(), with one parameter FOUND_ROWS(), GET_LOCK(), LAST_INSERT_ID(), LOAD_FILE(), MASTER_POS_WAIT(), NOW(), RAND(), RELEASE_LOCK(), SLEEP(), SYSDATE(), UNIX_TIMESTAMP(), USER(), UUID(), UUID_SHORT()**
* Do you know MySQL?
	* How would you backup and restore data using `mysqldump` from the command line?
	* When should you use SQL_CACHE and S_NO_CACHE on your queries?
	* Question: describe five functions that disable cache on queries and describe why. **Answer: BENCHMARK(), CONNECTION_ID(), CONVERT_TZ(), CURDATE(), CURRENT_DATE(), CURRENT_TIME(), CURRENT_TIMESTAMP(), CURTIME(), DATABASE(), ENCRYPT(), with one parameter FOUND_ROWS(), GET_LOCK(), LAST_INSERT_ID(), LOAD_FILE(), MASTER_POS_WAIT(), NOW(), RAND(), RELEASE_LOCK(), SLEEP(), SYSDATE(), UNIX_TIMESTAMP(), USER(), UUID(), UUID_SHORT()**
* PostgreSQL 관련 질문
	* [리소스 소비](http://www.postgresql.org/docs/current/static/runtime-config-resource.html)를 어떻게 개선시키는가?
* Do you know PostgreSQL?
	* How do you improve [Resource Consumption](http://www.postgresql.org/docs/current/static/runtime-config-resource.html)?
* SQL 서버
	* 어떻게 SQL 서버를 PostgreSQL이나 MySQL로 이전하겠는가?
* SQL Server
	* How would you migrate from SQL Server to PostgreSQL or MySQL?
* 추후에 번역 추가하도록 하겠습니다.
* Do you know How to 'hack', build a cluster, improve performance, implement cache, pooling or compile those services from source?
* NoSQL 데이터베이스에 대해서 얼마나 아는가?
* Are you familiar with NoSQL databases?

**[[⬆]](#toc) 목차로 되돌아가기**

###<a name="httpspecific">HTTP 관련 질문</a>

* 브라우저에 URL을 입력하고 요청한 페이지를 볼때까지 어떤 일이 일어나는가?
* What happens between the time you enter a URL in your browser until you see the page that you requested?
* 서버에 페이지를 요청했을때 TCP 3-way handshake가 어떻게 일어나는가?
* How does the 3-way TCP handshake occur when you request a page from a server?
* HTTP 요청과 응답 헤더에 어떤 내용이 들어가는가?
* What are the contents of an HTTP request header? Response header?
* HTTP와 HTTPS 프로토콜의 차이점은 무엇인가?
* What is the difference between HTTP and HTTPS?
* URL 축약서비스를 어떻게 설계하겠는가?
* How would you design a URL shortener similar to bit.ly?

**[[⬆]](#toc) 목차로 되돌아가기**

###<a name="ormspecific">ORM 관련 질문</a>

**[[⬆]](#toc) 목차로 되돌아가기**

###<a name="webservicesespecific">웹 서비스 관련 질문</a>

* 웹 서비스를 개발하거나 운영해본 경험이 있습니까?
* Have you created or managed some web service?
* 어떤 웹 서비스 프로토콜을 알고 있습니까?
* What web service protocals do you know?

####<a name="csrcspecific">Common Server Response Codes</a>

Question: Describe server response code 200. **Answer: ("OK") Evertying went ok. The entity-body, if any, is a representation of some resource.**

Question: Describe server response code 201. **Answer: ("Created") A new resource was created at the client's request. The location header should contain a URI to the new resource and the entity-body should contain a representation of the newly created resource.**

Question: Describe server response code 204. **Answer: ("No Content") The server declined to send back any status message or representation**

Question: Describe server response code 301. **Answer: ("Moved Permanently") Client triggered an action on the server that caused the URI of a resource to change.**

Question: Describe server response code 400. **Answer: ("Bad Request") A problem occured on the client side. The entity-body, if any, is a error message.**

Quesiton: Describe server response code 401. **Answer: ("Unauthorized") The client faild to provide proper authentication for the requested resource.**

Question: Descibe server response code 404. **Answer: ("Not Found") Client requested a URI that doesn't map to any resource.**

Question: Describe server response code 409. **Answer: ("Conflict") Client attempted to put the servers resource into a impossable or inconsistant state.**

Question: Descibe server response code 500 **Answer: ("Internal Server Error") A problem occured on the server side. The entity-body, if any, is a error message.**

**[[⬆]](#toc) return to Table of Contents**

###<a name="osespecific">Operating System Specific Questions</a>

* Linux/Unix/MacOS
	* Do you know how to use MacPorts, Aptitude, YUM, RPM and other package managers?
	* How often do you update running services?
	* How would you install, configure and handle services such nginx, apache, squid, samba, etc..?
	* What do you know about kernel tuning?
	* What do you know about virtualization?
	* What is the difference between threads and processes?
* Microsoft
	* How to remove Windows?
	* How would you install Linux using USB or liveCDs?
	* How would you disable Secure Boot and install Linux?
	* How would you migrate from windows to Linux?

**[[⬆]](#toc) return to Table of Contents**

###<a name="networkspecific">Network Specific Questions</a>

* What are the 7 layers of the OSI model?
* What are some advantages of CDNs? Disadvantages?
* What is a reverse proxy?
* What ports do the following use?
	* HTTP
	* HTTPS
	* SSH

**[[⬆]](#toc) return to Table of Contents**
	
