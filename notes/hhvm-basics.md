# HHVM Basics
> by: Sara Golemon  
> [http://joind.in/talk/view/13453][1]

* HHVM is not a source transformer (HPHPc)
* Runs your PHP pages live, just like PHP
* Uses standard FastCGI transport
* HHVM supports all PHP syntax
	* Tracking HEAD (mostly)
		* Splat & Variadics
		* Finally
		* Generators
		* Namespaces
	* PHP 7 features... (soon)
		* Null coalesce operator **??**
		* Spaceship operator **<=>**
	* And some of its own
		* Scalar type hint
		* Async co-routines
		* Generics
		* Collections (smart arrays)
		* XHP (Integrated XHTML)
		* User Attributes
		* Null-safe operator

[1]: http://joind.in/talk/view/13453