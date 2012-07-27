php-templates
=============

Maintenance release of php-templates, originally developed by Maxim Poltarak. Available at: http://sourceforge.net/projects/php-templates/

I was tasked with migrating an application running on PHP4 in FreeBSD 8.3 to PHP 5 in Ubuntu 12.04 and I found that it would not compile without some work. Since the project appears to have been abandoned years ago, I'm releasing the changes here.

I started with the last release 1.7.2, and applied the FreeBSD ports patches, available here: http://www.freebsd.org/cgi/cvsweb.cgi/ports/www/php-templates/

The remainder of the changes I made to cope with the deprecation of zend_get_parameters_ex(), replacing it with zend_parse_parameters().

Installation
============
- tar -zxf templates.tar.gz
- cd temlpates
- phpize
- ./configure --enable-templates=shared
- make
- make install
- Add extension=template.so in your php.ini
