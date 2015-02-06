# Keynote
> by: Rasmus Lerdorf

* 20 years of PHP!
	* PHP Announcement: June 8, 1995
	* Posted to `comp.infosystems.www.authoring.cgi`
* PHP 7
	* Engine improvements
		* Lower memory usage
		* Native threads
	* Returns AST (Need static analyzer)
	* Return types
		* `function name(): array { return []; }`
	* Null Coalesce Operator
		* `echo $a ?? $b;`
	* Removal of many deprecated features (PHP 4!)
	* 64-bit integer support on Windows
	* Cleanup edge-case integer overflow/underflow
	* Catchable `call to member function of non-object`
	* Uniform variable syntax
		* `$foo()['bar']()`
		* `getStr(){0}`
		* `$foo::$bar::$baz`
		* `foo()()`
		* `(...)()`
	* Unicode Codepoint Escape Syntax
	* ICU IntChar class added to intl extension
	* First RC scheduled for June 2015
	* Help test!
		* Vagrant image: [https://github.com/rlerdorf/php7dev][1]
		* Switch versions easily (20 pre-compiled version)
			* `sudo newphp 56 debug`
			* `sudo newphp 7`

[1]: https://github.com/rlerdorf/php7dev