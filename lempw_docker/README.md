# docker_wordpress_nginx_mariadb
Fully Dockerized Wordpress site leveraging Nginx, MariaDB, and PHP7.1

You can find an indepth set of instructions and a comprehensive tutorial here: http://outofmyhead.olssonandjones.com/2017/11/15/docker-wordpress-site-with-nginx/

It goes into great detail with regard to just about every possible configuration setting in this Docker project.



Setup: WordPress
We're almost complete here - now we just have to download the latest WordPress (currently located at https://wordpress.org/latest.tar.gz

Let's go ahead and download it now:

wget -O www/latest.tar.gz https://wordpress.org/latest.tar.gz
Next we'll untar/gunzip:

cd www
tar -xvzf latest.tar.gz
We could leave everything in the newly created wordpress directory or (as in this case) move it all to www root and remove wordpress directory. This really is a choice on how you want directory structures under www laid out:

mv wordpress/* ./
rmdir wordpress
rm latest.tar.gz​
Finally let's fix permissions on the host www directory:

chmod a+rwx -R ../www
