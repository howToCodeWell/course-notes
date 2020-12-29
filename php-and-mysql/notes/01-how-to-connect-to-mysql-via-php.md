---
course_slug: php-mysql
tutorial_number: 1
type: note
---

There are two ways to connect to MySQL via PHP using the MySQLi extension
- [Procedural](#procedural)
- [Object Oriented](#object-oriented)

Both require the hostname, username, and database parameters. The port and socket are optional

## Procedural

###  Connecting to the database
Here is an example of connecting to MySQLi using the `mysqli_connect` function

```php
$hostname = 'localhost';
$username = 'root';
$password = 'myPassword';
$database = 'my_db';
$port = 3306; // Optional
$socket = ''; //Optional
$connection = mysqli_connect($hostname, $username, $password, $database, $port);
```
###  Checking for connection errors
To check for a connection error use the `mysqli_connect_error` function. 

To get the error number call the `mysqli_connect_errno` function

```php
if(mysqli_connect_error()){
    die('Connection error '. mysqli_connect_errno() . ' ' . mysqli_connect_error());
}
```

### Closing the connection

To close the MySQL connection use the `mysqli_close` function passing in the `$connection` variable

```php
mysqli_close($connection);
```

## Object Oriented 

###  Connecting to the database
Here is an example of connecting to MySQLi using the `mysqli` object.  This will create a `mysqli` class instance

```php
$hostname = 'localhost';
$username = 'root';
$password = 'myPassword';
$database = 'my_db';
$port = 3306; // Optional
$socket = ''; //Optional

$connection = new mysqli($hostname, $username, $password, $database, $port, $socket);
```
###  Checking for connection errors

To check for a connection error use the `connect_error` property. 

To get the error number call the `connect_errno` property

```php
if($connection->connect_error){
    die('Connection error '. $connection->connect_errno . ' ' . $connection->connect_error);
}
```

### Closing the connection

To close the MySQL connection call the `close` method from the `mysqli` class instance

```php
$connection->close();
```
