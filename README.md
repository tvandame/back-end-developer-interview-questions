Back-End-Developer-Interview-Questions
======================================

A list of helpful back-end related questions you can use to interview potential candidates. 
Inspired by the git-repo: https://github.com/darcyclarke/Front-end-Developer-Interview-Questions.git and
[Paul Irish](http://paulirish.com) ([@paul_irish](http://twitter.com/paul_irish)) 

|Version    |Detail          |
|-----------|----------------|
|1.0.0      |Initial Draft   |

This repo contains a number of back-end interview questions that can be used when vetting potential candidates. 
It is by no means recommended to use every single question here on the same candidate (that would take hours). 
Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open ended and could lead to interesting discussions that tell 
you more about the person's capabilities than a straight answer would.

##Contributors

* [@travisvandame](http://www.twitter.com/travisvandame)

##General Questions:

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

## PHP Specific Questions

### PHP Code Examples:
```php
floor(3.14)
```
Question: What value is returned from the above statement?

**Answer: 3**

```php
$strText = "i'm a lasagna hog";

$strTmp = str_split($strText);
$strTmp = array_reverse($strTmp);
$strTmp = join("",$strTmp);

echo $strTmp;
```
Question: What value is returned from the above statement? 

**Answer: "goh angasal a m'i"**

```PHP
$array = array();

array_push($array, 1);
array_push($array, 2);
```
Question: What is the value of count($array);

**Answer: 2**

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
Question: What is the outcome of the two alerts above?

**Answer: alert_a() = Hello World, alert_b() = E_NOTICE : type 8 -- Undefined variable: foo -- at line 15 World**

## Database Specific Questions
* MySQL
* PostgreSQL
* SQL Server

## HTTP Specific Qustions

## Server Specific Qustions
* Linux/Unix
* Microsoft

## Web Services Specific Questions

### Common Server Response Codes

Question: Describe server response code 200

**Answer: ("OK") Evertying went ok. The entity-body, if any, is a representation of some resource.**

Question: Describe server response code 201

**Answer: ("Created") A new resource was created at the client's request. The location header should contain a URI to the new resource and the entity-body should contain a represntation of the newly created resource.**

Question: Describe server response code 204

**Answer: ("No Content") The server declined to send back any status message or representation** 

Question: Describe server response code 301

**Answer: ("Moved Permanently") Client triggered an action on the server that caused the URI of a resource to change.**

Question: Describe server response code 400

**Answer: ("Bad Request") A problem occured on the client side. The entity-body, if any, is a error message.**

Quesiton: Describe server response code 401

**Answer: ("Unauthorized") The client faild to provide proper authentication for the requested resource.**

Question: Descibe server response code 404

**Answer: ("Not Found") Client requested a URI that doesn't map to any resource.**

Question: Describe server response code 409

**Answer: ("Conflict") Client attempted to put the servers resource into a impossable or inconsistant state.**

Question: Descibe server response code 500

**Answer: ("Internal Server Error") A problem occured on the server side. The entity-body, if any, is a error message.**
