Back-End Job Interview Questions
================================

A list of helpful back-end related questions you can use to interview potential candidates.
Inspired by the git-repo: https://github.com/darcyclarke/Front-end-Developer-Interview-Questions.git and
[Paul Irish](http://paulirish.com) ([@paul_irish](http://twitter.com/paul_irish))

@Version 1.0.1

This repo contains a number of back-end interview questions that can be used when vetting potential candidates.
It is by no means recommended to use every single question here on the same candidate (that would take hours).
Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

##<a name="toc">Table of Contents</a>
* [Contributors](#contributors)
* [General Questions](#general)
* [Specific Questions](#specific)
* [Code examples](#codeexamples)
* [Database Specific Questions](#databasespecific)
* [HTTP Specific Questions](#httpspecific)
* [Operating System Specific Questions](#osespecific)
* [Web Services Specific Questions](#webservicesespecific)
	* [Common Server Response Codes Specific Questions](#csrcspecific)
* [Network Specific Questions](#networkspecific)

###<a name="contributors">Contributors</a>

* [@travisvandame](http://twitter.com/travisvandame)
* [@jmurowaniecki](http://twitter.com/jmurowaniecki)
* [@toothpaste_](http://twitter.com/toothpaste_)
* [@emanuelsaringan](http://twitter.com/emanuelsaringan)

**[[⬆]](#toc) return to Table of Contents**

###<a name="general">General Questions</a>

* What did you learn yesterday/this week?
* What excites or interests you about coding?
* What version control systems have you used (Git, SVN etc.)?
* What is your preferred development environment? (OS, Editor, Browsers, Tools etc.)
* How do you go about testing your PHP?
* Have you ever looked at the source code of the libraries/frameworks you use?
* How do you organize your code?
* When do you optimize your code?
* If you could master one technology this year what would it be?
* Explain the importance of standards and standards bodies.
* Explain MVC, HMVC, his differences, goals and cons.
* What did you learn/know about agile methodology?
* Do you prefer to work on a team or alone?
* What's the biggest problem faced on your projects and how did you solve it?
* How you contribute to the open source community (Github, Bitbucket, IRC, foruns)?

**[[⬆]](#toc) return to Table of Contents**

###<a name="specific">PHP Specific Questions</a>

* Describe two good uses - and pratices - for callback usage.

**[[⬆]](#toc) return to Table of Contents**

###<a name="codeexamples">PHP Code Examples:</a>

```php
floor(3.14)
```
Question: What value is returned from the above statement? **Answer: 3**

```php
echo join("", array_reverse(str_split("i'm a lasagna hog")));
```
Question: What value is returned from the above statement? **Answer: "goh angasal a m'i"**

```PHP
$array = array();

array_push($array, 1);
array_push($array, 2);
```
Question: What is the value of `count($array)`? **Answer: 2**

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
Question: What is the outcome of the two alerts above? **Answer: alert_a() = Hello World, alert_b() = E_NOTICE : type 8 -- Undefined variable: foo -- at line 15 World**

**[[⬆]](#toc) return to Table of Contents**

###<a name="databasespecific">Database Specific Questions</a>

* General SQL
	* What is the difference between a View and a Table?
	* What does the HAVING clause do?
	* How do you choose a column to be indexed?
* Do you know MySQL?
	* How would you backup and restore data using `mysqldump` from the command line?
	* When should you use SQL_CACHE and S_NO_CACHE on your queries?
	* Question: describe five functions that disable cache on queries and describe why. **Answer: BENCHMARK(), CONNECTION_ID(), CONVERT_TZ(), CURDATE(), CURRENT_DATE(), CURRENT_TIME(), CURRENT_TIMESTAMP(), CURTIME(), DATABASE(), ENCRYPT(), with one parameter FOUND_ROWS(), GET_LOCK(), LAST_INSERT_ID(), LOAD_FILE(), MASTER_POS_WAIT(), NOW(), RAND(), RELEASE_LOCK(), SLEEP(), SYSDATE(), UNIX_TIMESTAMP(), USER(), UUID(), UUID_SHORT()**
* Do you know PostgreSQL?
	* How do you improve [Resource Consumption](http://www.postgresql.org/docs/current/static/runtime-config-resource.html)?
* SQL Server
	* How would you migrate from SQL Server to PostgreSQL or MySQL?
* Do you know How to 'hack', build a cluster, improve performance, implement cache, pooling or compile those services from source?

**[[⬆]](#toc) return to Table of Contents**

###<a name="httpspecific">HTTP Specific Questions</a>

* What happens between the time you enter a URL in your browser until you see the page that you requested?
* How does the 3-way TCP handshake occur when you request a page from a server?
* What are the contents of an HTTP request header? Response header?
* What is the difference between HTTP and HTTPS?

**[[⬆]](#toc) return to Table of Contents**

###<a name="webservicesespecific">Web Services Specific Questions</a>

* Have you created or managed some web service?
* What web service protocals do you know?

####<a name="csrcspecific">Common Server Response Codes</a>

Question: Describe server response code 200. **Answer: ("OK") Evertying went ok. The entity-body, if any, is a representation of some resource.**

Question: Describe server response code 201. **Answer: ("Created") A new resource was created at the client's request. The location header should contain a URI to the new resource and the entity-body should contain a represntation of the newly created resource.**

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
	* How often you updates the service of its customers?
	* How would you install, configure and handle services such ngynx, apache, squid, samba, etc..?
	* What do you know about kernel tuning?
	* What do you know about virtualization?
* Microsoft
	* How to remove Windows?
	* How would you install Linux using USB or liveCDs?
	* How would you disable Secure Boot and install Linux?
	* How are your adaptation to Linux?

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
