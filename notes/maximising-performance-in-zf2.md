# Maximising Performance in ZF2
> by: Gary Hockin  
> [http://joind.in/talk/view/13458][1]

* Tool for Performance Testing
	* [Siege][2] or ab
		* e.g. `siege -c 10 -t 1m -b http://local.veo.tv/`
	* [Xdebug][3] or xhprof
		* Use [Webgrind][4] for Xdebug profile processing.
* Use Opcode Cache (OpCache)
* Use [EdpSuperluminal][5]
	* Combines all used Zend component classes into one file.
	* Consider generating this cache in your deployment strategy.
* Configuration Caching
* Routing
	* The ordering of your routes matter (FILO). Most important routes should be at the bottom of the array.
	* Module ordering counts too when it comes to the routing tree.
* View Template Map
	* Generate a view template map for each module.
	* `php ../../bin/template_generator.php`
* Class Map
	* Generate a class file map for each module.
	* `php ../../bin/classmap_generator.php`
* Best Practices
	1. Don't use closures in module.config.php
	2. Replace closures with Factory classes
	3. Minimize use of the EventManager
	4. Cache all the things (memcached, etc)

[1]: http://joind.in/talk/view/13458
[2]: http://www.joedog.org/siege-home
[3]: http://xdebug.org/docs/install
[4]: https://github.com/jokkedk/webgrind
[5]: https://github.com/EvanDotPro/EdpSuperluminal