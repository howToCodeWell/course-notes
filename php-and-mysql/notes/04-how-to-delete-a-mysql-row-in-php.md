To delete a record from a MySQL database run the following:

```sql
DELETE FROM `users` WHERE `id` = '123'
```
This can be done in PHP using MySQLi like so

```php
$sql = "DELETE FROM `users` WHERE `id` = '123'";
$connection = new mysqli('hostname', 'username', 'password', 'my_db');
$hasDeleted = $connection->query($sql);
if($hasDeleted) {
    echo 'Record has been deleted';
} else {
    echo 'record still exists';
}
$connection->close();
```

