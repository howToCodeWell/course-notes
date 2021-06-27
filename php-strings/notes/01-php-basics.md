## PHP Beginners Course Strings Tutorial #1 Basics


## Starting a PHP Script


To start a PHP script you need to open up a blank file in your editor and start the file with a PHP tag: 

```php
<?php

```


It is also possible to use capitals instead:

```php
<?PHP

```


It is recommended that you remain consistent with your use of capitalization across your files.
Note that you don't need to close the PHP tag. It is advisable that you don't close the tag if you don't need to as it can cause further issues.


## Variables

To create a variable, you need a dollar symbol at the start of the variable name.
At the end of the variable name, you add an equals symbol to assign a value. For a string value, you can wrap a string value in either a single or double quote. You can't mix quote types at the start and the end of the string.
The statement must end with a semi-colon.

For example, to create a variable named 'temp' with a value of "test", you would end up with a script of:

```php
<?php

$temp = "test";
```


Alternatively you can use single quotes, as follows:

```php
<?php

$temp = 'test';
```

Save the file with the filename of 'tutorial1.php'.

If you run the file in the terminal at present, the program won't give you any visual results.
For example, if you enter the following in the terminal to run the program, nothing will happen:

php -f tutorial1.php

This won't print anything out to the screen. At the moment the script just assigns a value and does not display any result on screen.

To display the value on the screen, we will need to use either the echo or print command.
echo is an internal PHP call we can use to print something out to the screen.
Remember to add the semi-colon to the end of the line. If you forget a semi-colon at the end of your statements you will receive a syntax error on-screen.

```php
<?php

$temp = "test";

echo $temp;
```


Save the script as tutorial1.php.
Run the file in the terminal by typing in the following:

php -f tutorial1.php

The script will display the value of test in the command line, but as we have not entered any new line formatting the value will display next to the prompt.

To make the program insert a new line, we can use the code of '\n' to insert a new line. To add a new line at the beginning and end of the string, we do the following:

```php
<?php

$temp = "\ntest\n";

echo $temp;
```


Now save and run the script in the command prompt to see the result.
To insert another new line at the end of the string, we can add another '\n':

```php
<?php

$temp = "\ntest\n\n";

echo $temp;
```


Note that although you can use either double or single quotes to encapsulate a string, the behaviour of '\n' is different when using single quotes.
If you use single quotes, PHP will output the string as it was typed in typed rather than interpreting the code as a new line and inserting a new line. For example, running the following script of:

```php
<?php

$temp = '\ntest\n\n';

echo $temp;
```


Will output a result of:

\ntest\n\n


## Joining Strings


Concatenation is the joining of strings to make a single string.
You need to use a period symbol to join two variables together.

```php
<?php

$firstName = "Peter";
$lastName = "Fisher";
$fullName = $firstName . $lastName;

echo $fullName;
```

Save and run the script again.

You will notice that when the value is output, the resulting string that is output is on a single line and contains no spacing or new lines.
Change the script to the following to add a new line to the end of the string.

```php
<?php

$firstName = "Peter";
$lastName = "Fisher";
$fullName = $firstName . $lastName . "\n";

echo $fullName;
```

Save and run the script.

Now the string has one new line at the end. We can alter the script as follows to insert extra new lines to improve the screen formatting.

```php
<?php

$firstName = "Peter";
$lastName = "Fisher";
$fullName = "\n" . $firstName . $lastName . "\n\n";

echo $fullName;
```

To fix the spacing we need to add a space between the $firstName and $lastName variables:

```php
<?php

$firstName = "Peter";
$lastName = "Fisher";
$fullName = "\n" . $firstName . " " . $lastName . "\n\n";

echo $fullName;
```

Save and run the script.



## Integer Variables

To assign an integer value to a variable in PHP, you need to indicate that the name you are using is a variable by using the dollar symbol.
As an integer is a number value, you shouldn't wrap the value in quotes. For example, to assign a number to a variable named $age, you would enter the following:
 
```php
<?php

$firstName = "Peter";
$lastName = "Fisher";
$age = 32;

$fullName = "\n" . $firstName . " " . $lastName . "\n\n";

echo $fullName;
```


Amend the script to remove the existing variable of $fullName and replace it with the variable of $profile. We can now change the output to display the age variable value:

```php
<?php

$firstName = "Peter";
$lastName = "Fisher";
$age = 32;

$profile = "\nFull Name: " . $firstName . " " . $lastName . "\n\n" . "Age: " . $age . "\n";

echo $profile;
```


The previous example is not as easy to read, due to the length of the line and the '\n' codes at different points.
To resolve this problem we can amend the script.

```php
<?php

$firstName = "Peter";
$lastName = "Fisher";
$age = 32;

$profile = "\nFull Name: " . $firstName . " " . $lastName . "\n\n";
$profile .= "Age: " . $age . "\n\n";

echo $profile;
```


Save and run the script.


The period symbol and the equals symbol combined is a shorthand equivalent of typing:

$profile = $profile . "Age: " . $age . "\n\n";


We can make the script easier to read by making use of further concatenation and substituting the double new line string with a new variable named $nb :

```php
<?php

$title = "Mr";
$firstName = "Peter";
$lastName = "Fisher";
$age = 32;
$nb = "\n\n";

$profile = "\n";
$profile .= "Full Name: " . $title . " " . $firstName . " " . $lastName . $nb;
$profile .= "Age: " . $age . $nb;

echo $profile;
```


To improve the script we can add a variable that contains a telephone number: 

```php
<?php

$title = "Mr";
$firstName = "Peter";
$lastName = "Fisher";
$age = 32;
$telephone = "123456789652";
$nb = "\n\n";

$profile = "\n";
$profile .= "Full Name: " . $title . " " . $firstName . " " . $lastName . $nb;
$profile .= "Age: " . $age . $nb;
$profile .= "Telephone: " . $telephone . $nb;

echo $profile;
```

Save and run the script to output the data.


## Subjects covered

* Strings and concatenation in PHP
* How we concatenate strings together into a longer string
* New lines and breaking lines up
* Differences between using single and double quotes in strings.

