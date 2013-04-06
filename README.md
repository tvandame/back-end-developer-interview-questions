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

* [@travisvandame](http://www.twitter.com/travisvandame) - http://www.leandertechnologies.com

##General Questions:

* What version control systems have you used (Git, SVN etc.)?
* What is your preferred development environment? (OS, Editor, Browsers, Tools etc.)
* Explain how Object inheritance works. [Answer](http://php.net/manual/en/language.oop5.inheritance.php)

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
Question: Question: What is the outcome of the two alerts above?
**Answer: alert_a() = Hello World, alert_b() = E_NOTICE : type 8 -- Undefined variable: foo -- at line 15 World**

## ASP .NET Specific Questions

### Language
* C#

## Database Specific Questions
* MySQL
* PostgreSQL
* SQL Server

## HTTP Specific Qustions

## Server Specific Qustions
* Linux/Unix
* Microsoft

## Webservice Specific Qustions
* JSON
* XML
* SOAP
