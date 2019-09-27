# What is PingMeLive?

This is a library which helps you to get LIVE notifications of actions taking place on your webistes and applications.
Just Copy past the below codes and get live updates of errors and actions. Make Categories of pings based on projects (etc) and assign it to your team mates.
That's what PING ME LIVE does.
Easy right!.

## How to use

### Register yourself on
[https://pingmelive.com](https://pingmelive.com)
You will get your API KEY after registeration.


### Usage

Include pingmelive
```php
<?php
require_once("pingmelive.lib.php");
$pingmelive = new pingMeLive("apiKey","projectID","errorStatus(true/false)","errorName"); 
?>

```

...and you are done!

## Custom Events

You can also use pingMeLive for sending custom events.

### 1.Simple event
```php
<?php 
//To trigger Simple Event, Just call the below function.
$pingMeLive->simpleEvent("groupTitle","eventMessage");
?>
 ```    

If you want to send some detailed long description you can use `Detailed event`
### 2.Detailed event
```php
<?php 
//To trigger Detailed Event, Just call the below function.
$pingMeLive->detailedEvent("groupTitle","eventMessage","detailDescription");
?>
```

### Options
* **apiKey** : You will get an `API KEY` when you will register on pingmelive.com
* **projectID** : Once registered, Click on New Project to create. 
* **errorStatus** : `true` / `false` (Boolen Value).
* **errorName** : This will be your `Group Title/Name` where all the error will be pinged.(This works when `errorStatus` is set as `true`.
* **groupTitle** : This will be your `Group Tilte/Name` under which , you will get all your pings.
* **eventMessage** : The `errorMessage` is limited to 360 character in length. Any additional characters beyond 360 character will be truncated.
* **detailDescription** : The `detailDescription` is does not have any length limitation. You can also send JSON Formatted String / or simple plain string.

## Some usefull information

* If you only want error pings, Just install the library and and intialize it.
* You can smartly use group title for you custom events.

