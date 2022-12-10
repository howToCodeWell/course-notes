A conditional statement changes the flow of the application based on the evaluation of a condition.

There are three types of conditional statements in PHP
1. if statement
2. if else statement
3. if elseif else statement

## 1. If statement
An if statement consists of the conditional statement and the body.  The body will get executed if the conditional statement is true.
```php
if ($conditionToCheck) {
    // Statement body.
    // This gets executed when the $conditionToCheck is true
}
```

The example below will output `It is ready` because the variable `$isReady` is evaluated to true.
```php
$isReady = true;
if ($isReady === true) {
    // This will run as $isReady is true
    echo "It is ready";
}
```
The example below will not output `It is ready` because the variable `$isReady` is evaluated to false.
```php
$isReady = false;
if ($isReady === true) {
    // This will not run as $isReady is false
    echo "It is ready";
}
```

## 2. If else statement
An if else statement consists of the conditional statement and a else block. The else block is executed if the conditional statement is not met.

```php
if ($conditionToCheck) {
    // Statement body.
    // This gets executed when the $conditionToCheck is true
} else {
    // else block.
    // This gets executed when the $conditionToCheck is false
}
```

The example below will set the value of `$settings['api_key]` to `abc_test` because the `$mode` has the value of `test`.
```php
$settings = [
    'api_key' => 'abc_dev'
];

$mode = 'test';
if ($mode === 'prod') {
    $settings = ['api_key'] = 'abc_prod'
} else {
    $settings = ['api_key'] = 'abc_test'
}

```
## 3. If elseif statement
An if elseif statement consists of the conditional statement, an elseif block and a else block. The elseif block is executed if the first conditional statement has not been met but its condition has been met.

The else block gets executed when the if condition or the elseif condition has not been met.

```php
if ($valueToCheck) {
    // Statement body.
    // This gets executed when the $valueToCheck is true
} elseif($anotherValueToCheck) {
    // elseif block
    // This gets executed when the $valueToCheck is false but the $anotherValueToCheck condition is true 
} else {
    // else block.
    // This gets executed when the $valueToCheck and the $anotherValueToCheck are both false
}
```

The example below will set the value of `$discountAmount` to `20` because the `$discountCode` has the value of `HOWTOCODEWELL`. 

In this example the `elseif` block is executed as the if condition has not met but the `elseif` condition is correct. 

```php
$discountCode = 'HOWTOCODEWELL';

if ($discountCode === 'BLACKFRIDAY') {
    $discountAmount = 10;
} elseif($discountCode === 'HOWTOCODEWELL') {
    $discountAmount = 20; 
} else {
    $discountAmount = 0; 
}
```

If there are many possible values for `$discountCode` then a switch statement would be recommended.