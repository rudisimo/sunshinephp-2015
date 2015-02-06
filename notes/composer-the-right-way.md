# Composer The Right Way
> by: Rafael Dohms  
> [http://joind.in/talk/view/13445][1]

* Library Publishers
	* Join a collective (The League of Extraordinary Packages)
* Use tilde operator `~` for proper minor/patch version control.
	* `~1.2` === `>=1.2.0, <2.0.0`
	* `~2.0.1` === `>=2.0.1, <2.1.0`
* **New** caret operator `^` follow actual semantic versioning rules.
	* `^1.2.3` === `>=1.2.3, <2.0.0`
* Cleaning up `composer.lock` file.
	* `composer update --lock`
* Check your third-party licenses.
	* `composer licenses`
* Use a proxy for private packages.
	* [Satis][2]
	* [Toran][3]
* Use [pickle][4] instead of PECL.

[1]: http://joind.in/talk/view/13445
[2]: https://getcomposer.org/doc/articles/handling-private-packages-with-satis.md
[3]: http://toranproxy.com
[4]: https://github.com/FriendsOfPHP/pickle