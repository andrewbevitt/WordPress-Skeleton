# WordPress Skeleton

This is forked from [markjaquith/WordPress-Skeleton](https://github.com/markjaquith/WordPress-Skeleton).

Primary change is to use my own WP fork as the `/wp/` submodule. This contains some changes to enable SSL connections to the MySQL database where certificates are required. This introduces some optional extra configuration options:

* MYSQL_SSL_KEY - Path to the client key file
* MYSQL_SSL_CERT - Path to the client certificate
* MYSQL_SSL_CA - Path to the server CA certificate
* MYSQL_SSL_CAPATH - Path to directory containing CA certificates
* MYSQL_SSL_CIPHER - String list of valid ciphers to include

A ticket is open for these changes to be merged upstream [here](https://core.trac.wordpress.org/ticket/28625).

## Assumptions

* WordPress as a Git submodule in `/wp/`
* Custom content directory in `/content/` (cleaner, and also because it can't be in `/wp/`)
* `wp-config.php` in the root (because it can't be in `/wp/`)
* All writable directories are symlinked to similarly named locations under `/shared/`.

