A switch consists of one or many cases that are checked against a supplied value.
Much like a series of if statements a switch can include a default that is used when the supplied value does not match any case.

In the example the printed string would say `This fruit is a pear` as the variable `$fruit` has the value of `pear`.

If the supplied `$fruit` does not match any of the case conditions then the output would be `The fruit cannot be found`.

```php
$fruit = 'pear';

switch ($fruit) {
    case 'apple':
        echo "This fruit is an Apple";
    break;
    case 'pear':
        echo "This fruit is a pear";
    break;
    case 'orange':
        echo "This fruit is an orange";
    break;
    default:
        echo "The fruit cannot be found";
}

```

This example can also be written using a series of if/if else/else statements.
```php
if ($fruit === 'apple') {
    echo "This fruit is an Apple";
} elseif ($fruit === 'pear') {
    echo "This fruit is a pear";
} elseif ($fruit === 'orange') {
    echo "This fruit is an orange";
} else {
    echo "The fruit cannot be found";
}
```

Switch cases can be grouped together.

In the below example below the output would be `This food is a meat` as `$food` has the value of `beef burger`.

If `$food` had the value of `apple` or `pear` or `orange` then the output would be `This food is a fruit`

```php
$food = 'beef burger';

switch ($food) {
    case 'apple':
    case 'pear':
    case 'orange':
        echo "This food is a fruit";
    break;
    case 'beef burger': 
       echo "This food is a meat";
    break;
    default:
        echo "The fruit cannot be found";
}
```

The equivalent if statement would look like this

```php
if ($food === 'apple' || $food === 'pear' || $food === 'orange') {
    echo "This food is a fruit";
} elseif ($food === 'beef burger')  {
    echo "This food is a meat";
} else {
    echo "The fruit cannot be found";
}
```
