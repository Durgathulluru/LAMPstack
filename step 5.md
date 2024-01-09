# STEP 5 — ENABLE PHP ON THE WEBSITE

With the default DirectoryIndex settings on Apache, a file named index.html will always take precedence over an index.php file.
This is useful for setting up maintenance pages in PHP applications, by creating a temporary index.html file containing an
informative message to visitors. Because this page will take precedence over the index.php page, it will then become the landing
page for the application. Once maintenance is over, the index.html is renamed or removed from the document root, bringing back the
regular application page.


In case you want to change this behavior, you’ll need to edit the /etc/apache2/mods-enabled/dir.conf file and change the order in 
which the index.php file is listed within the DirectoryIndex directive:


```
sudo vim /etc/apache2/mods-enabled/dir.conf
```

```
<IfModule mod_dir.c>
        #Change this:
        #DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
        #To this:
        DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
```

After saving and closing the file, you will need to reload Apache so the changes take effect:


```
sudo systemctl reload apache2
```

Finally, we will create a PHP script to test that PHP is correctly installed and configured on your server.

Now that you have a custom location to host your website’s files and folders, we’ll create a PHP test script to confirm that 
Apache is able to handle and process requests for PHP files.

Create a new file named index.php inside your custom web root folder:

```
vim /var/www/projectlamp/index.php
```

This will open a blank file. Add the following text, which is valid PHP code, inside the file:

```
<?php
phpinfo();
```
When you are finished, save and close the file, refresh the page and you will see a page similar to this:


![projject1-step5](https://user-images.githubusercontent.com/85270361/210115357-dfca0250-7e0b-4f3c-8e26-8266be9cc4a6.PNG)

If you can see this page in your browser, then your PHP installation is working as expected.
