백앤드 개발자 면접 문제 은행
======================================

@Version 1.0

이 저장소에는 백앤드 개발자 면접에 나왔던 문제들이 있습니다.
여기에 있는 모든 문제들은 푸는 것(꽤 많은 시간이 걸릴 것입니다)보다는
여기서 몇 가지 질문을 골라 자신의 실력을  평가해보는 것이 좋을 것입니다.

## 한국어 번역

* [@DevSusu](https://github.com/DevSusu)

## <a name="toc">목차</a>
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

### <a name="contributors">기여자</a>

* [@travisvandame](http://twitter.com/travisvandame)
* [@jmurowaniecki](http://twitter.com/jmurowaniecki)
* [@emanuelsaringan](http://lambdageek.com)

**[[⬆]](#toc) 목차로 되돌아가기**

### <a name="general">일반 질문</a>

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

### <a name="dpspecific">디자인 패턴 관련 질문</a>

* <a name="mvcspecific">MVC</a>
* <a name="mvvmspecific">MVVM</a>
* <a name="repospecific">레파지토리 패턴</a>
* <a name="dispecific">의존성 주입</a>
* <a name="vspecific">방문자 패턴</a>
    * 이 패턴에 들어가는 클래스와 객체들은 무엇이 있는가? **답변: Visitor, ConcreteVisitor, Element, ConcreteElement, ObjectStructure**

**[[⬆]](#toc) 목차로 되돌아가기**

### <a name="phpcodeexamples">PHP 코드 예제:</a>

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

### <a name="phpspecific">PHP 관련 질문</a>

* 콜백을 쓰는 두 가지 좋은 실례를 설명하시오.

**[[⬆]](#toc) 목차로 되돌아가기**

### <a name="databasespecific">데이터베이스 관련 질문</a>

* 일반 SQL
	* 뷰와 테이블의 차이점이 무엇인가?
	* HAVING 문이 하는 일이 무엇인가?
	* 인덱싱할 열을 어떻게 선택하는가?
* MySQL 관련 질문
	* 당신은 어떻게 커맨드 라인을 사용하여 mysqldump로부터 데이터를 백업하고 복구하겠는가?
	* 어떤 상황에서 SQL_CACHE와 S_NO_CACHE를 쿼리에서 쓸 것인가?
	* 질문: 캐시를 불활성화하는 5개의 함수를 설명하고 왜 그런지도 설명하라.
		**답변: BENCHMARK(), CONNECTION_ID(), CONVERT_TZ(), CURDATE(), CURRENT_DATE(), CURRENT_TIME(), CURRENT_TIMESTAMP(), CURTIME(), DATABASE(), ENCRYPT(), with one parameter FOUND_ROWS(), GET_LOCK(), LAST_INSERT_ID(), LOAD_FILE(), MASTER_POS_WAIT(), NOW(), RAND(), RELEASE_LOCK(), SLEEP(), SYSDATE(), UNIX_TIMESTAMP(), USER(), UUID(), UUID_SHORT()**
* PostgreSQL 관련 질문
	* [리소스 소비](http://www.postgresql.org/docs/current/static/runtime-config-resource.html)를 어떻게 개선시키는가?
* SQL 서버
	* 어떻게 SQL 서버를 PostgreSQL이나 MySQL로 이전하겠는가?
* 추후에 번역 추가하도록 하겠습니다.
* Do you know How to 'hack', build a cluster, improve performance, implement cache, pooling or compile those services from source?
* NoSQL 데이터베이스에 대해서 얼마나 아는가?

**[[⬆]](#toc) 목차로 되돌아가기**

### <a name="httpspecific">HTTP 관련 질문</a>

* 브라우저에 URL을 입력하고 요청한 페이지를 볼때까지 어떤 일이 일어나는가?
* 서버에 페이지를 요청했을때 TCP 3-way handshake가 어떻게 일어나는가?
* HTTP 요청과 응답 헤더에 어떤 내용이 들어가는가?
* HTTP와 HTTPS 프로토콜의 차이점은 무엇인가?
* URL 축약서비스를 어떻게 설계하겠는가?

**[[⬆]](#toc) 목차로 되돌아가기**

### <a name="ormspecific">ORM 관련 질문</a>

**[[⬆]](#toc) 목차로 되돌아가기**

### <a name="webservicesespecific">웹 서비스 관련 질문</a>

* 웹 서비스를 개발하거나 운영해본 경험이 있습니까?
* 어떤 웹 서비스 프로토콜을 알고 있습니까?

#### <a name="csrcspecific">대표적 서버 응답 코드</a>

질문: 서버 응답 코드 200에 대해서 설명하라. **답변: ("OK") 모든 과정이 잘 처리되었다. body가 있을 경우 리소스를 표현하는 것이다.**

질문: 서버 응답 코드 201에 대해서 설명하라. **답변: ("Created") 새로운 리소스가 생성되었다. location 헤더는 리소스를 가르키는 URI를 포함하고 있어야 하고 body는 새로 생성된 리소스의 대표값을 가진다.

질문: 서버 응답 코드 204에 대해서 설명하라. **답변: ("No Content") 서버가 어떠한 상태 메세지를 보내기를 거부하였다.**

질문: 서버 응답 코드 301에 대해서 설명하라. **답변: ("Moved Permanetly") 클라이언트가 리소스의 URI를 바꾸도록 하였다.**

질문: 서버 응답 코드 400에 대해서 설명하라. **답변: ("Bad Request") 클라이언트에서 문제가 발생했다. body가 에러 메세지이다.**

질문: 서버 응답 코드 401에 대해서 설명하라. **답변: ("Unauthorized") 클라이언트가 요청한 리소스에 대한 적절한 인증 조건을 만족하지 못하였다.**

질문: 서버 응답 코드 404에 대해서 설명하라. **답변: ("Not Found") 클라이언트가 어떠한 리소스에도 해당하지 않는 URI를 요청했다.**

질문: 서버 응답 코드 409에 대해서 설명하라. **답변: ("Conflict") 클라이언트가 서버의 리소스를 접근 불가능하거나 동기화되지 않은 상태로 바꾸려고 하였다.**

질문: 서버 응답 코드 500에 대해서 설명하라. **답변: ("Internal Server Error") 서버에서 문제가 발생하였다. body는 에러 메세지이다.**

**[[⬆]](#toc) 목차로 되돌아가기**

### <a name="osespecific">운영체제 관련 질문</a>

* Linux/Unix/MacOS
	* MacPorts, Aptitude, YUM, RPM과 같은 패키지 매니저를 쓰는 방법을 아십니까?
	* 이미 진행되고 있는 서비스를 어떻게 업데이트 합니까?
	* nginx, apache, squid, samba 와 같은 서비스를 설치하고 설정하며 관리합니까?
	* 커널 튜닝에 대해 아십니까?
	* 가상화에 대해서 아십니까?
	* 프로세스와 쓰레드의 차이점은 무엇입니까?
* Microsoft
	* 윈도우를 삭제하는 방법은?
	* USB나 liveCD를 이용하여 리눅스를 설치하는 방법은?
	* 어떻게 Secure Boot를 해제하고 리눅스를 설치하겠는가?
	* 윈도우에서 리눅스로 어떻게 이전하겠는가?

**[[⬆]](#toc) 목차로 되돌아가기**

### <a name="networkspecific">네트워크 관련 질문</a>

* OSI 모델의 7 계층은 무엇인가?
* CDN의 장점과 단점에 대해 설명하시오.
* What are some advantages of CDNs? Disadvantages?
* Reverse Proxy가 무엇인가?
* 아래 프로토콜에 사용되는 포트는?
	* HTTP
	* HTTPS
	* SSH

**[[⬆]](#toc) 목차로 되돌아가기**