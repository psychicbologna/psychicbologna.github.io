https://1stwebdesigner.com/local-web-server/

1 - https://www.apachelounge.com/download/ install the vc_redist and the apache zip with its config file. Check the windows version for appropriate version.
2 - Append Path environment variable to include c:\apache\bin.
3 - Configure settings in the httpd config file:
ServerRoot to proper root for Apache
4 - Open cmd.exe as admin, enter ‘httpd -k install’
5 - Attempt to run the app using ‘httpd -k start’ or checking Services.
6 - Install PHP with config file and add its directory to Path environment, test with ‘cmd php -version’ and index.php of dev\www folder.
7 - Install MySQL with a custom install, making sure in advanced options to set the right path and configuration settings (Firewall exception, include bin in path, launch automatically). Write down root password.
8 -  Install PhpMyAdmin into the www\pma folder.


WINDOWS .net framework 3.5 must be installed through “windows features” for wix.exe to work

(this adds http://php.net/manual/fa/install.windows.apache2.php updated Apache loadmodule, last updated 2018)

*Don’t forget environment variables in the Path for Apache, PhP, MySQL and PhpMyAdmin.

cmd:

httpd -k start/stop/restart to run Apache
php -v to test a php connection and see version.

Php needs mbstring active and all extension paths need to lead to the proper places.
