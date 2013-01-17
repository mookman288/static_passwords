# Static Passwords

## Developed by PxO Ink (http://pxoink.net/)

### Preface

Static Passwords is designed to generate a password, with 
numbers, (optional) characters, and whole words from a 
/usr/share/dict/words file, from a Debian 5 install. 

The inspiration for this application comes from two sources: 
(1) the xkcd comic about [password strength](http://xkcd.com/936/), 
and (2) a call for new and interesting things on the web. 

Concerning the xkcd comic, I understand that the whole point 
is to create a password which you can easily remember, and the 
truth is, this generator will not do that. However, concerning 
creating something interesting... There's tons of password 
generators out there, but there are few that have some weird 
niche, like using whole words, or being compiled into a class 
for PHP. So, there you have it. Constructive criticism welcome.

### Efficiency

It's not efficient. It's slow, and clunky. It weighs 707 KB. When 
it comes to efficiency, I urge you to fork your own and innovate. 
It's currently setup so that all of the words are loaded in through 
an array. The `array_rand` function is used to pull words. Some 
`mt_rand` functions determine if a word should be capitalized, 
or if a number or character should be injected.

### Implementation and Customization

Static Passwords can be called with the following code:

```php
	<?php
		//Require the static passwords component.
		require_once('static-passwords.php');
		
		//Instantiate the class.
		$password	=	new staticPasswords();
		
		//Print the generated password.
		print($password -> generate());
	?>
```

There are optional parameters which can be set:

* Password strength (integer)
* Use of random characters (boolean)

```php
		//Print the generated password.
		print($password -> generate(6, false));
```

### Compatibility

PHP 5.3+

### License

*The MIT License (MIT)*

Software Copyright &copy; 2013 PxO Ink. Most Rights Reserved.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.