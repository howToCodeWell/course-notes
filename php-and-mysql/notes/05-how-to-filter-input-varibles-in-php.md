To filter user input use the `filter_input` function.
This function takes 4 parameters and returns a mixed response.
`filter_input ( int $type , string $var_name , int $filter = FILTER_DEFAULT , array|int $options = 0 ) : mixed`

1) `type`

This could be `INPUT_GET`, `INPUT_POST`, `INPUT_COOKIE`, `INPUT_SERVER` or `INPUT_ENV`

2)`var_name`

This is the variable name to get.

3) `filter`

This is the ID of the filter that you want to use.  `FILTER_DEFAULT` is used by default

4) `options`

An array of options that you wish to supply to the filters. This could also be bitwise disjunction of flags.

## Examples

### Filtering an email address from a `POST` request. 
Using the `FILTER_SANITIZE_EMAIL` filter will remove any invalid characters

```php
$email = '   a£(@b).com';
$_POST['email_address'] = $email;
$filtered = filter_input(INPUT_POST, 'email_address', FILTER_SANITIZE_EMAIL);
print $filtered;
// a@b.com
```

### Validating an email address from a  `POST` request.

Using the `FILTER_VALIDATE_EMAIL` filter will return true if the email address is valid and false if not.

```php
$email = 'a.com';
$_POST['email_address'] = $email;
$isValid = filter_input(INPUT_POST, 'email_address', FILTER_VALIDATE_EMAIL);
var_dump($isValid);
// bool(false)
```


### Requiring an array in a `GET` request
```php
$_GET['selection'] = [
    'choice_1' => ['a', 'b', 'c'],
    'choice_2' => ['x', 'y', 'z'],
];
$isValid = filter_input(INPUT_GET, 'selection', FILTER_DEFAULT, FILTER_REQUIRE_ARRAY);
var_dump($isValid);
// bool(true)
```

### Applying a default value to an array from a `GET` request
```php
// Notice that $_GET isn't supplied with 'age' so the default will be used.
$options = [
    'options' => [
        'default' => 5
    ]
];
$value = filter_input(INPUT_GET, 'age', FILTER_VALIDATE_INT, $options);
var_dump($value);
// int(5)
```
### Applying a max and min range of values
```php
// As the $age is less than the min_range $isValid is false.
$age  = 3;
$_GET['age'] = $age;
$options = [
    'options' => [
        'min_range' => 10,
        'max_range' =>  4
    ]
];
$isValid = filter_input(INPUT_GET, 'age', FILTER_VALIDATE_INT, $options);
var_dump($isValid);
// bool(false)
```


