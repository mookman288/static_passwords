# Static Passwords
## Developed by PxO Ink (http://pxoink.net/)

## Preface

Static Passwords is designed to generate a complex password with numbers, characters, and whole words from a Debian 5 based words file.

The goal is to take a complex password and obfuscate it using a much smaller "normal" looking password. For instance, this library could generate the following password:

    38 agglutinated ^ Epidermal 4 Finesses 25 motive 6 Percentile Porters quartering 55 Razzed

Which could then be shortened and written down:

    38a^E4F25m6PPq55R

The inspiration for this application comes from three sources:

1. An xkcd comic about [password strength](http://xkcd.com/936/)
2. A lengthily paper written for university on the topic of password strength in comparison to length and complexity
3. The goal to create something that can trigger the memory of a long, complex password (previously known as a call for new and interesting things on the Web)

Concerning the xkcd comic, I understand the original intention was to create a password which can be easily remembered. The idea here is to do the same, but take a more active role in understanding that password length and character complexity is an important and necessary pre-requisite to achieve. This password generator is an inefficient (700KB+) way to merge those two worlds. Feel free to fork your own version.

## Implementation and Customization

Static Passwords can be called with the following code:

```php
		//Require the static passwords component.
		require_once('static-passwords.php');

		//Instantiate the class.
		$password	=	new staticPasswords();

		//Print the generated password.
		print($password -> generate());
```

There are optional parameters which can be set:

* Password strength (integer)
* Use of random complex characters (boolean)

```php
		//Print the generated password.
		print($password -> generate(6, false));
```

## Compatibility

PHP 5.3+

## License

*The MIT License (MIT)*

Software Copyright &copy; 2013 PxO Ink. Most Rights Reserved.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.