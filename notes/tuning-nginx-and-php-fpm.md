# Tuning Nginx And PHP-FPM The Right Way
> by: Evan Coury  
> [http://joind.in/talk/view/13439][1]

* Was Nginx's logo inspired by Top Gun?
* Nginx
	* `/etc/sysctl.conf`
		* `fs.file-max=131072` 256 per MB of (available) RAM
		* `net.ipv4.tcp_tw_recycle = 1`
		* `net.ipv4.tcp_tw_reuse = 1`
		* `net.core.somaxconn = 1024`
		* `net.ipv4.ip_local_port_range = 1024 65535`
	* `/etc/nginx/nginx.conf`
		* `worker_rlimit_nofile 100000`
		* `worker_processes auto`
		* `worker_connections 40000`
		* `events { use epoll; }`
		* `events { multi_accept on; }`
		* `events { sendfile on; tcp_nopush on; }`
* PHP-FPM
	* Stick to TCP Sockets
	* `/etc/php-fpm.conf`
		* `events.mechanism = epoll`
		* `rlimit_files = 100000`
		* `pm = static`
		* `pm.max_children = 64`
		* `pm.max_requests = 1000`
	* Don't use `memcached` for session management, use `phpredis`
* (Maybe) Put logs in memory `/dev/shm/nginx-access.log`
* Don't gzip compressed formats (PNG, JPEG, GIF)
* Ansible playbook can be found [here][2]

[1]: http://joind.in/talk/view/13439
[2]: https://github.com/EvanDotPro/nginx-php-fpm-tuning