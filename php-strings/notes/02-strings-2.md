---
course_slug: php-strings
tutorial_number: 2
type: note
---
## PHP Beginners Course Strings Tutorial #2

## Manipulating Strings


Type in the following PHP script:

```php

<?php
$temp = "The Cat Is Sat On The Mat";
echo $temp;
echo "\n";
```

Save the file with the filename of tutorial1.php

Run the file from the prompt using the command:

php -f tutorial1.php

The file should run and output the string "The Cat Is Sat On The Mat" to the screen.


## Counting the Amount of Characters

We can count the number of characters in the string by using the strlen function.

PHP has a number of string manipulation functions. Functions starting with 'str' are usually those that manipulate strings.

In the example, we are trying to find the length of the string named $temp. so we write this as:

```php
strlen($temp);
```

We want to echo this out to the screen, so we type echo at the front of the statement:

```php
echo strlen($temp);
```

Example script:

```php
<?php

$temp = "The Cat Is Sat On The Mat";
echo strlen($temp);
echo "\n";
```

When you run this, the script outputs to the screen an integer of 25, which is the total number of characters in the string.
Note that the function also counts the number of spaces contained in the string.

To demonstrate, if we add extra spaces to the string, the number of characters counted will increase:

```php
<?php

$temp = "     The Cat Is Sat On The Mat      ";
echo strlen($temp);
echo "\n";
```

Note that strlen will count the number of space characters in the string, even if they are at the beginning or end.

If we change the script to echo out the contents of the $temp string to screen, we can see that strlen does not remove any spaces:

```php
<?php

$temp = "     The Cat Is Sat On The Mat      ";
echo $temp;
echo "\n";
echo strlen($temp);
echo "\n";
```

If we run the script you will see that the spaces are still present in the output.

We can use the function named trim to remove spaces from a string that appear at the beginning and the end of a string. Trim can also be used for removing other characters, but by default it is used for removing space characters.

This script displays the string $temp stripped of spacing from the beginning and end of the string. We can also combine the function with strlen to output the number of characters in the trimmed string:


```php
<?php

$temp = "     The Cat Is Sat On The Mat      ";
echo trim($temp);
echo "\n";
echo strlen(trim($temp));
echo "\n";
```

Running the script will demonstrate that the number of characters returned is now 25.

Trim is a useful function for when you are dealing with user input from forms on your website. It can help sanitize user input as it can remove a users' mistyped spacing.



## Accessing a Character's Position within a String

We can do this by treating the string as an array and accessing the index in the string.
For example, the second character in the $temp string is the letter 'h'. If we want access the second character from the $temp string by its position, we start our counting from the index number of zero. Therefore the first character at position one is at index number zero and the second character is located at index number one.

The following demonstrates how the index of the $temp is numbered:

 | Char | Index No. |
 |:---:|:---:|
 |T|0|  
 |h|1|  
 |e|2|
 ||3|
 |C|4| 
 |a|5|
 |t |6|
 ||7|
 |I|8|
 |s|9|
 ||10|
 
...etc

To echo out the value of $temp found at index one we use the following instruction:

```php
echo $temp[1];
```

We can run the script:

```php
<?php

$temp = "The Cat Is Sat On The Mat      ";
echo $temp[1];
echo "\n";
echo strlen(trim($temp));
echo "\n";
```

This will return the value of 'h'.

If we change the index value in the $temp variable to two, the script will return 'e' which is the third character:

```php
<?php

$temp = "The Cat Is Sat On The Mat      ";
echo $temp[2];
echo "\n";
echo strlen(trim($temp));
echo "\n";
```

## Capitalization of a String

At present, each word contained in the $temp string is a capital letter, whereas other letters are lowercase.

To change the case of the entire $temp string to lowercase, we use the function strtolower.
To use the function, we place the variable that we want to change in the parentheses:

```php
strtolower($temp);
```

The following script demonstrates:

```php
<?php

$temp = "The Cat Is Sat On The Mat";

echo "\n";
echo strtolower($temp);
echo "\n";
```

When run, the script will output the string:

'the cat is sat on the mat'

The opposite of strtolower is the function strtoupper. This will convert the string to uppercase, as shown below:

```php
<?php

$temp = "The Cat Is Sat On The Mat";

echo "\n";
echo strtoupper($temp);
echo "\n";
```

Running this script will output the string 'THE CAT IS SAT ON THE MAT'.


## Splitting a String

To split a string down into individual words, we use the function explode.
This function will take the contents of the string and place it into an array, with each element of the array containing each individual word. It requires that at a minimum, you specify the name of the string you want to split and the character that you want to split the string by(delimiter).
The most common delimiter that you will want to use is the space character, as this is what usually separates the words in a string.
A third parameter is available, where you can set a limit to the number of words returned.

For example, to output the string contained in the $temp variable into individual words, we can write:

```php
echo explode(" ", $temp);
```

The first parameter specifies the delimiter and the second is the name of the variable.

As we want to output the contents of an array, we can make this easier to read when the data is output. To do this we can output an HTML tag named pre to the output:

```php
print "<pre>";  
```

When we output the array to the screen, we should do this by using the function print_r:

```php
print_r(explode(" ", $temp));
```

To keep the HTML valid, we should close off the pre tag:

```php
print "</pre>";`
```

We can write this to a script as follows:

```php
<?php

$temp = "The Cat Is Sat On The Mat";

print "<pre>";
print_r(explode(" ", $temp));
print "</pre>";
```

When you run the script, the result returned will be:

```php
<pre>Array
{
	[0] => The
	[1] => Cat
	[2] => Is
	[3] => Sat
	[4] => On
	[5] => The
	[6] => Mat
}
</pre>
```

If we assign the value to an array, we can echo out an element of the array by passing in an index number:

```php
<?php

$temp = "The Cat Is Sat On The Mat";

$arr = explode(" ", $temp);
echo $arr[1];
echo "\n";
```

This will return the second element in the array (remember that the index starts at zero, so we pass in a value of one for the second element).
The word 'Cat' will be output.

Changing the index value in the array to six will output the seventh entry ('Mat').

```php
<?php

$temp = "The Cat Is Sat On The Mat";

$arr = explode(" ", $temp);
echo $arr[6];
echo "\n";
```

Functionality is present in PHP to output the last index value in an array without specifying an index number. To do this, we use the function named end and supply the array variable:

```php
<?php

$temp = "The Cat Is Sat On The Mat";

$arr = explode(" ", $temp);
echo end($arr);
echo "\n";
```

