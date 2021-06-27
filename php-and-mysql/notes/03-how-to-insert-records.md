The following SQL will insert a record in a MySQL table

```sql
INSERT INTO `tbl_user` (`first_name`, `last_name`)
VALUES ('Peter', 'Fisher');
```

To do this in PHP first make a connection to the database and then run a insert query

```php
$insertSQL = "INSERT INTO `tbl_user` (`first_name`, `last_name`) VALUES ('Peter', 'Fisher')";

$connection = new mysqli('hostname', 'username', 'password', 'my_db');
$hasInserted = $connection->query($insertSQL);
if($hasInserted === true) {
    echo 'Record has been inserted into the database';
} else {
    echo 'Record has not been inserted';
}
$connection->close();
```

To insert multiple records use an array of data and concatenate the insert SQL

```php
$userData = [
    [
        'first_name' => 'Peter',
        'last_name' => 'Fisher'
    ],
    [
        'first_name' => 'John',
        'last_name' => 'Smith'
    ]
];
$insertSQL = "INSERT INTO `tbl_user` (`first_name`, `last_name`) VALUES ";
$userCount = count($userData);
foreach($userData as $key => $user) {
    $counter = ($key +1);
    $insertSQL.=" ('".$user['first_name']."' , '".$user['last_name']."') ";
    $insertSQL.= ($counter < $userCount) ? " , " : "";
}
$connection = new mysqli('hostname', 'username', 'password', 'my_db');

$hasInserted = $connection->query($insertSQL);
if($hasInserted === true) {
    echo $userCount.' record(s) has been inserted into the database';
} else {
    echo 'Records have not been inserted';
}
$connection->close();
```
