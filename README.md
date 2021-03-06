# Sanitize String Class

[![Version](https://poser.pugx.org/vgd/sanitize_string/version)](//packagist.org/packages/vgd/sanitize_string) [![Total Downloads](https://poser.pugx.org/vgd/sanitize_string/downloads)](//packagist.org/packages/vgd/sanitize_string) [![Latest Unstable Version](https://poser.pugx.org/vgd/sanitize_string/v/unstable)](//packagist.org/packages/vgd/sanitize_string) [![License](https://poser.pugx.org/vgd/sanitize_string/license)](//packagist.org/packages/vgd/sanitize_string)

Sometimes you may want to clean a filename or string from foreign languages characters; with this class you can do both.


## Usage

```
Install via composer:

composer require vgd/sanitize_string

or

require('SanitizeString.php');


The class uses two boolean parameters after the string/filename: 

The first one (isFileName) is used to tell the class that you are trying to clean a file name.

The second one (special) must be used if you would like to remove special characters as well from a 
string or a file name.

```

### In order to clean a string:

```
To remove foreign characters only:

echo SanitizeString::clean('Your string here');


To remove foreign AND special characters:

echo SanitizeString::clean('Your string here', false, true);

```


### In order to clean a filename:

```
To remove foreign characters only:

SanitizeString::clean('Your filename here', true, false);


To remove foreign AND special characters:

SanitizeString::clean('Your filename here', true, true);


You can use absolute or relative paths for the file you want to rename.

```


### Final Note

```
The main purpose of using associative arrays and not other techniques as regular 
expressions and preg_match etc. was to give the user the possibility of add or remove
characters depending of their needs.

Lets say that you have a spanish text and you want to remove all the characters but vowels 
with tilde and ñ characters; you can modify the arrays to achieve that.

```
