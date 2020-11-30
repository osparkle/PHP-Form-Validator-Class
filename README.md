# PHP-Form-Validator-Class
PHP class for validating HTML form fields and form data submitted for processing. It performs most of the validations you will ever need.

It is compatible with PHP 7.3.0

# Sample Usage

include "PHP_Form_Validator.php";

$validate = Validator();

$validate->name('Full Name')->value($fullname)->pattern('words')->min(3)->max(64)->required();

$validate->name('Email Address')->value($email)->pattern('email')->min(11)->max(80)->required();

$pass1 = 'password1';
$validate->name('Password')->value($pass1)->pattern('text')->min(6)->max(32)->required();

$pass2 = 'password2';
$validate->value($pass1)->confirmPass($pass2);
