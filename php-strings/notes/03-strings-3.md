## PHP Beginners Course Strings Tutorial #3

## Capitalizing the First Letter in the First Word Within a String


Type in the following PHP script:

```php

<?php
$temp = "i am a long string";
echo $temp;
echo "\n";
```

Save the file with the filename of tutorial1.php

Run the file from the prompt using the command:

php -f tutorial1.php

The file should run and output the string "i am a long string" to the screen.

In the example, the first word is in lowercase. This does not follow the rules of capitalization in a written sentence, as the first letter in the first word must always be a capital letter.
To correct this we use the function `ucfirst()`. The 'uc' part of the function name stands for 'UpperCase'.

To use `ucfirst()`, we pass in a variable into the parenthesis. In the example, this will be $temp:

```php
ucfirst($temp);
```

Our script should be altered as follows to introduce this function:

```php

<?php
$temp = "i am a long string";
echo ucfirst($temp);
echo "\n";
```

Save the file with the filename of tutorial1.php

Run the file from the prompt using the command:

php -f tutorial1.php

The file should run and output the string "I am a long string" to the screen.
You will notice that the letter 'i' at the start point of the string is now output as a capital letter.


## Capitalizing the First Letter in all of the Words Within a String

Back in the second tutorial in this series, the functions `toupper()` and `tolower()` were introduced. The function `toupper()` turned the whole string to uppercase, whereas `tolower()` turned the whole string to lowercase.
If we only want to turn the first letter of each word in a string to uppercase, we use the function `ucwords()`.

To use `ucwords()`, we pass in a variable into the parenthesis. In the example script, this will be $temp:

```php
ucwords($temp);
```

We can use this in our script like so:

```php

<?php
$temp = "i am a long string";
echo ucwords($temp);
echo "\n";
```

If we run the script, the output will now be "I Am A Long String".

## Changing the First Letter in a String to Lowercase

To change the first letter in a string to lowercase, the function `lcfirst()` is used.

To show this in action we will need to change the $temp variable to include a capital letter at the start of the string. We also need to amend the script to use the `lcfirst()` function.

Amend the script as follows:

```php

<?php
$temp = "I am a long string";
echo lcfirst($temp);
echo "\n";
```

Running this script will demonstrate the `lcfirst()` function and will output the $temp string with a lowercase 'i' at the beginning.

We can also combine the functions `lcfirst()` and `ucwords()` to convert the first letter of each word in the string to uppercase, but leaving the first letter of the string as lowercase.
To do this, amend the script to read:

```php

<?php
$temp = "I am a long string";
echo lcfirst(ucwords($temp));
echo "\n";
```


## Wrapping Words at Set Positions Within a String

You may come across a scenario when you are outputting content to a web page, that you need to ensure that a line of text does not exceed the width of the container. This could result in the text overlapping into an area of the page where it shouldn't be and breaking your page design.
To overcome this problem, you may want to wrap the text at a set point or prevent the text from displaying past a certain number of characters.
To resolve this issue, we can use the function `wordwrap()`.

The function requires at least one argument, namely the name of the string you want to wrap.

The second argument is optional and is the character width at which the word should be wrapped.

If we pass in the arguments $temp and 2, the function will wrap the string at the end of the word plus a space character, where a word reaches a count of 2 characters or less.
If the word exceeds 2 characters, then a space will not be included at the end of the word.

Amend the script as follows to demonstrate:

```php

<?php
$temp = "I am a long string";
echo wordwrap($temp, 2);
echo "\n";
```

The output should read:

I  
am  
a  
long  
string  

Note that with the smaller words that are wrapped, space characters are included at the end of the line where the word is two characters or less.

A third optional argument can be added that supplies the function with the character(s) we want to display at the breaking point. As an example, we could insert a line break character.

A fourth optional boolean argument is available to strictly cut words at the set point that you have supplied. 'true' to cut words, 'false' to leave whole words uncut.

The next script shows the examples given in action:

```php

<?php
$temp = "I am a long string";
echo wordwrap($temp, 2, "\n", true);
echo "\n";
```

The output will show:

I  
am  
a  
lo  
ng  
st  
ri  
ng  

 
The supplied second argument does not have to be a single character. It can also be a string:

```php

<?php
$temp = "I am a long string";
echo wordwrap($temp, 2, " ... ", true);
echo "\n";
```

The script shown will output the following:

I ... am ... a ... lo ... ng ... st ... ri ... ng

To summarize, the arguments for `wordwrap()` are:

Type | Required / Optional | Description
:-----:|:---------------------:|:------------
String | Required | The name of the string you want to wrap
Integer| Optional | The character width at which the word should be wrapped (default is 75 characters)
String |  Optional |  The character or characters we want to be displayed at the breaking point
Boolean |  Optional |  Whether whole words should be cut at the set point supplied.  'true' to cut words, 'false' to leave whole words uncut. Default is 'false'. 

