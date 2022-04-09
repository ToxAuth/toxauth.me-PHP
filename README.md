# ToxAuth Php Example


This is the official Php Example for [ToxAuth](https://toxauth.me).
For more information, please visit [Documenatation](https://setup.toxauth.me).



### Init API
---
```php
require 'toxauth.php';

$auth_instance = new toxauth\api("VERSION", "PROGRAM KEY", "API / ENC KEY");
```

### Login User
---
```php
require 'toxauth.php';

$auth_instance = new toxauth\api("VERSION", "PROGRAM KEY", "API / ENC KEY");

if (isset($_POST['submit'])) {
    $logged_in = $auth_instance->login($_POST['username'], $_POST['password']);

    if ($logged_in) {
        print_r($_SESSION["user_data"]);

        exit;
    }
}
```

### Register User
---
```php
require 'toxauth.php';

$auth_instance = new toxauth\api("VERSION", "PROGRAM KEY", "API / ENC KEY");

if (isset($_POST['submit'])) {
    $logged_in = $auth_instance->register($_POST['username'], $_POST['email'], $_POST['password'], $_POST['token']);

    if ($logged_in) {
        print_r($_SESSION["user_data"]);

        exit;
    }
}
```

### Activate
---
```php	
require 'toxauth.php';

$auth_instance = new toxauth\api("VERSION", "PROGRAM KEY", "API / ENC KEY");

if (isset($_POST['submit'])) {
    $logged_in = $auth_instance->activate($_POST['username'],  $_POST['token']);

    if ($logged_in) {
        print_r($_SESSION["user_data"]);

        exit;
    }
}
```

### All in one
---
```php
require 'toxauth.php';

$auth_instance = new toxauth\api("VERSION", "PROGRAM KEY", "API / ENC KEY");

if(isset($_POST['submit'])){
	$logged_in = $auth_instance->all_in_one($_POST['token']);

	if($logged_in){
		print_r($_SESSION["user_data"]);

   		exit;
	}
}
```

### Log 
---
```php
require 'toxauth.php';

$auth_instance = new toxauth\api("VERSION", "PROGRAM KEY", "API / ENC KEY");

if(isset($_POST['submit'])){
	$logged_in = $auth_instance->log($_POST['username'], $_POST['message']);

	if($logged_in){
		print_r($_SESSION["user_data"]);

   		exit;
	}
}
```

