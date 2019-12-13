hxpro.nginx
===========

[![Build Status](https://travis-ci.org/hxpro/ansible-role-nginx.svg?branch=master)](https://travis-ci.org/hxpro/ansible-role-nginx)

Nginx - this role is under development.

Requirements
------------

This role will define only default server configuration.
You can put your own configuration here `/etc/nginx/conf.d/`.
Add default content to here `/var/www/html/`


Role Variables
--------------

```
nginx_worker_connections: 1024
nginx_client_max_body_size: 1m
nginx_ipv6: False
# on (default), off, build
nginx_server_tokens: "on"
nginx_modules:
  - http-image-filter
  - http-perl
  - http-xslt-filter
  - mail
  - stream
nginx_default_root: /var/www/html
nginx_default_conf: True
nginx_gzip_types:
  - text/xml
  - text/plain
  - text/css
  - text/javascript
  - application/json
  - application/x-javascript
  - application/javascript
  - application/xml
  - application/xml+rss
  - application/xhtml+xml
  - application/rss+xml
nginx_http_header: []
# Default value should be True, False for backward compatibility
nginx_fastcgi_request_buffering: False
```

Dependencies
------------

 - hxpro.epel


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: hxpro.nginx }

License
-------

WTFPL

Author Information
------------------

Matěj Koudelka <matej@hxpro.cz>
