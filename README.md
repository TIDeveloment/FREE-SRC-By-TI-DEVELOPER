# Src Web Develoment v1

## เว็บไซต์นี้เขียนโดย
```js
PHP , SQL , PDO , CSS , JS
```

## Getting Started
**First, clone this Template**
<hr>

```php
https://github.com/TIDeveloment/FREE-SRC-By-TI-DEVELOPER.git
```

### connection.php
<hr>

```php
<?php 

    $conn = mysqli_connect("localhost", "root", "", "Database");

    if (!$conn) {
        die("Failed to connec to databse " . mysqli_error($conn));
    }

?>
```

### config.php
<hr>

```php
<?php 

    $db_host = "localhost";
    $db_user = "root";
    $db_password = "";
    $db_name = "Database";

    try {
        $db = new PDO("mysql:host={$db_host}; dbname={$db_name}", $db_user, $db_password);
        $db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    } catch(PDOEXCEPTION $e) {
        $e->getMessage();
    }


?>
```
