The following SQL will select records from a MySQL table

```sql
SELECT * FROM `tbl_user`;
```

To do this in PHP using MySQLi, first make a connection to the database and then run the select query

```php
$insertSQL = "SELECT `first_name`, `last_name` FROM `tbl_user`";

$connection = new mysqli('hostname', 'username', 'password', 'my_db');
$result = $connection->query($insertSQL);

if ($result->num_rows > 0) {
  // output data of each row
  while($row = $result->fetch_assoc()){
    echo "First name: " . $row["first_name"]."</br>";
    echo "Last name: " . $row["last_name"]."</br></br>";
  }
} else {
  echo "0 results";
}
$connection->close();
```
