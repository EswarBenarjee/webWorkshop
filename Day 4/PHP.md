# PHP 
### Personal Home Page ⬇️
### HyperText Preprocessor
- _Server Side Scripting Language_
- _Programming Language_
- _Open Source_
- _Case Insensitive_

### Xampp 
- _Open source cross-platform web server_
- _Developed by Apache_
- _PHP, MySQL_

### PHP Syntax
> _Can contain text, HTML, CSS, JavaScript, and PHP code_
```php
<?php
    PHP Code
?>
```

### PHP Commments
```php
    // This is a single-line comment

    # This is also a single-line comment

    /*
    This is a multiple-lines comment block
    that spans over multiple
    lines
    */
```

### PHP Variables
> _Always starts with $, and then the variable name_
```php
    $txt = "Hello there!";
    $x = 5;
    $y = 10.5;
```

### PHP Echo
> _Prints the value_
```php
    echo 'Hi';
    echo 'Hi', 'Hello';
```

### PHP Print
> _Prints the value and returns 1 if printed successfully_
```php
    print 'Hi';
```

### PHP Types
_Boolean, Integer, Float(same as Double, real), String, Array, Object, NULL, Resource_


### PHP gettype()
> _Returns the type of the variable_

```php
    echo gettype(5.5);
    echo gettype('Hi');
    echo gettype(5.'Hi');
    echo gettype('Hi'.5);
```

# PHP Strings
> 'This is valid' <br>
> "This is also valid" <br>
    
```php
    echo 'Hi Eswar' . '<br>';
    echo "Hi Eswar" . '<br>';
    echo "Hi 'Eswar'"  . '<br>';
    echo 'Hi "Eswar"' . '<br>';
    echo "Hi \"Eswar\"" . '<br>';; 
    echo "\"Hi Eswar\" " . '<br>';
    echo 'Hi \\Eswar' . '<br>';
    echo "Hi \Eswar" . '<br>';
```

### PHP String Length()
> _Returns length of a string_
```php
    echo strlen('I know spellings');
```

### PHp String Word Count()
> _Returns the number of words in a string_
```php
    echo str_word_count('I know spellings');
```

### PHP String Reverse()
> _Reverses a string_
```php
    echo strrev('I know spellings');
```

### PHP String Search()
> _Searches for a specific text within a string_
```php
    echo strpos('I know spellings', 'know');
```

### PHP String Replace()
> _Replaces some characters with some other characters in a string_
```php
    echo str_replace('know', 'knows', 'I know spellings');
```

### PHP explode
> _Splits a string into an array_
```php
    $str = 'Eswar,Abhiram,Narayana,Sriram';
    print_r(explode(',', $str));
```

### PHP implode
> _Joins array elements with a string_
```php
    $arr = ['Eswar', 'Abhiram', 'Narayana', 'Sriram'];
    echo implode(',', $arr);
```

### PHP String to Lower()
> _Converts a string to lowercase_
```php
    echo strtolower('ESWAR');
```

### PHP String to Upper()
> _Converts a string to uppercase_
```php
    echo strtoupper('eswar');
```

# PHP Arrays
```php
    // Index Based Array
    $cars = array("Volvo", "BMW", "Toyota");

    $cars = ["Volvo", "BMW", "Toyota"];

    // Associative Array
    $cars = ["Eswar"=>10, "Sriram"=>20, "Narayana"=>5, "Abhiram"=>1];

    // Multi Dimensional Array
    $cars = [
        ["Volvo", 10, 20],
        ["BMW", 20, 30],
        ["Toyota", 30, 40]
    ];
```

>  _Access Array Elements:_
```php
    $arr=array("a","b","c","d");
    echo $arr[1];
```

> _Set Array Elements:_
```php
    $cars = ["Volvo", "BMW", "Toyota"];
    $cars[0] = "Mini";
    echo $cars[0];
```

> _Loop Through an Indexed Array:_
```php
    $cars = ["Volvo", "BMW", "Toyota"];
    $arrlength = count($cars);

    // Index Based Array
    for($x = 0; $x < $arrlength; $x++) {
        echo $cars[$x];
        echo "<br>";
    }

    foreach($cars as $car) {
        echo $car;
        echo "<br>";
    }
```

> _Loop Through an Associative Array:_
```php
    $cars = ["Eswar"=>10, "Sriram"=>20, "Narayana"=>5, "Abhiram"=>1];

    foreach($cars as $key => $value) {
        echo "Key=" . $key . ", Value=" . $value;
        echo "<br>";
    }
```

# PHP Operators
> _Concatenation Operator_
```php
    $txt1 = "Hello";
    $txt2 = " world!";
    echo $txt1 . $txt2;
```

> _Assignment Operators_
```php
    $x = 10;
```

> _Arithmetic Operators_
```php
    +
    -
    *
    /
    %
    **
```

> _Comparison Operators_
```php
    ==
    ===
    !=
    <>
    !==
    <
    >
    <=
    >=
```

> _Increment/Decrement Operators_
```php
    ++
    --
```

> _Logical Operators_
```php
    and &&
    or ||
    xor
    !
```

# PHP Super Globals
> _PHP Superglobals are built-in variables that are always available in all scopes_
```php
    $GLOBALS
    $_SERVER
    $_REQUEST
    $_POST
    $_GET
    $_FILES
    $_ENV
    $_COOKIE
    $_SESSION
```

## $GLOBALS
> _Gets the element from GLOBAL Scope_
```php
    $x = 10;
    $y = 20;

    function add() {
        echo $GLOBALS['x'] + $GLOBALS['y'];
    }

    add();
```

```php
    $x = 10;
    $y = 20;

    function add() {
        $z = 40;
        echo $GLOBALS['x'] + $GLOBALS['y'] + $GLOBALS['z']; // Returns Error
    }

    add();
```

## $_SERVER
> _Gets the element from SERVER Scope_
```php
    echo $_SERVER['PHP_SELF'] . "</br>";
    echo $_SERVER['SERVER_NAME'] . "</br>";
    echo $_SERVER['HTTP_HOST'] . "</br>";
    echo $_SERVER['HTTP_USER_AGENT'] . "</br>";
    echo $_SERVER['SCRIPT_NAME'] . "</br>";
```

## $_REQUEST
> _Gets the element from REQUEST Scope_
```php
    echo $_REQUEST['name'] . "</br>";
    echo $_REQUEST['age'] . "</br>";
```

## $_GET
> _Uses data from URL_
```php
    echo $_GET['name'] . "</br>";
    echo $_GET['age'] . "</br>";
```

## $_POST
> _Encoded data that was sent to the page is used_
```php
    echo $_POST['name'] . "</br>";
    echo $_POST['age'] . "</br>";
```

## $_SESSION
> _Session variables are set in a page and are available to all pages in one application_
```php
    session_start();
    $_SESSION['name'] = 'Eswar';
    $_SESSION['age'] = 10;
```

## isset
> _Checks if a variable is set or not_
```php
    $name = 'Eswar';
    if(isset($name)) {
        echo 'Name is set';
    } else {
        echo 'Name is not set';
    }
```

# PHP Date
> _Returns the current date and time_
```php
    echo date('d-m-Y h:i:s');
```

> _Returns the current date_
```php
    echo date('d-m-Y');
```

> _Returns the current time_
```php
    echo date('h:i:s');
```

> _Returns the current day_
```php
    echo date('l');
```

> _Returns the current month_
```php
    echo date('F');
```

## Set Time Zone
> _Sets the default timezone used by all date/time functions in a page_
```php
    date_default_timezone_set('Asia/Kolkata');
    echo date('d-m-Y h:i:s');
```

# Include Files
> _Includes and evaluates the specified file_
```php
    include 'header.php';
```

> _Includes and evaluates the specified file_
```php
    include_once 'header.php';
```

# PHP JSON
> _Encodes a value to JSON format_
```php
    $arr = array("Eswar", "Sriram", "Narayana", "Abhiram");
    echo json_encode($arr);
```

> _Decodes a JSON string_
```php
    $json = '{"Eswar":10,"Sriram":20,"Narayana":5,"Abhiram":1}';
    $obj = json_decode($json);
    echo $obj->Eswar;
```

# Fetch Assoc
> _Fetches a result row as an associative array_
> Key is the column name, Value is the value in row.
```php
    $row = mysqli_fetch_assoc($result);
```

# MYSQL Database
```php
    PHP can connect to MySQL database using MySQLi OOPS or MySQLi Procedural or PDO
    We will MySQLi Procedural 
```

### Connect to Database
```php
    $servername = "localhost";
    $username = "root";
    $password = "";
    $dbname = "myDB";

    // Create connection
    $conn = mysqli_connect($servername, $username, $password, $dbname);

    // Check connection
    if (!$conn) {
        die("Connection failed: " . $conn->connect_error);
    }
    echo "Connected successfully";
```

### Run Insert Query
```php
    $sql = "INSERT INTO web VALUES (DEFAULT, 'Eswar', 20)";
    if (mysqli_query($conn, $sql)) {
        echo "New record created successfully";
    } else {
        echo "Error: " . $sql . "<br>" . $conn->error;
    }
```

### Run Select Query
```php
    $sql = "SELECT * FROM web";
    $result = mysqli_query($conn, $sql);

    if (mysqli_num_rows($result) > 0) {
        // output data of each row
        while($row = mysqli_fetch_assoc($result)) {
            echo "id: " . $row["id"]. " - Name: " . $row["name"]. " " . $row["age"]. "<br>";
        }
    } else {
        echo "0 results";
    }
```

