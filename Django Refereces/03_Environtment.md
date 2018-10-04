Django - Environment
Advertisements
 Previous Page Next Page  
Django development environment consists of installing and setting up Python, Django, and a Database System. Since Django deals with web application, it's worth mentioning that you would need a web server setup as well.

Step 1 – Installing Python
Django is written in 100% pure Python code, so you'll need to install Python on your system. Latest Django version requires Python 2.6.5 or higher

If you're on one of the latest Linux or Mac OS X distribution, you probably already have Python installed. You can verify it by typing python command at a command prompt. If you see something like this, then Python is installed.

$ python
Python 2.7.5 (default, Jun 17 2014, 18:11:42)
[GCC 4.8.2 20140120 (Red Hat 4.8.2-16)] on linux2
Otherwise, you can download and install the latest version of Python from the link http://www.python.org/download.

Step 2 - Installing Django
Installing Django is very easy, but the steps required for its installation depends on your operating system. Since Python is a platform-independent language, Django has one package that works everywhere regardless of your operating system.

You can download the latest version of Django from the link http://www.djangoproject.com/download.

UNIX/Linux and Mac OS X Installation
You have two ways of installing Django if you are running Linux or Mac OS system −

You can use the package manager of your OS, or use easy_install or pip if installed.

Install it manually using the official archive you downloaded before.

We will cover the second option as the first one depends on your OS distribution. If you have decided to follow the first option, just be careful about the version of Django you are installing.

Let's say you got your archive from the link above, it should be something like Django-x.xx.tar.gz:

Extract and install.

$ tar xzvf Django-x.xx.tar.gz
$ cd Django-x.xx
$ sudo python setup.py install
You can test your installation by running this command −

$ django-admin.py --version
If you see the current version of Django printed on the screen, then everything is set.

Note − For some version of Django it will be django-admin the ".py" is removed.

Windows Installation
We assume you have your Django archive and python installed on your computer.

First, PATH verification.

On some version of windows (windows 7) you might need to make sure the Path system variable has the path the following C:\Python34\;C:\Python34\Lib\site-packages\django\bin\ in it, of course depending on your Python version.

Then, extract and install Django.

c:\>cd c:\Django-x.xx
Next, install Django by running the following command for which you will need administrative privileges in windows shell "cmd" −

c:\Django-x.xx>python setup.py install
To test your installation, open a command prompt and type the following command −

c:\>python -c "import django; print(django.get_version())"
If you see the current version of Django printed on screen, then everything is set.

OR

Launch a "cmd" prompt and type python then −

c:\> python
>>> import django
>>> django.VERSION
Step 3 – Database Setup
Django supports several major database engines and you can set up any of them based on your comfort.

MySQL (http://www.mysql.com/)
PostgreSQL (http://www.postgresql.org/)
SQLite 3 (http://www.sqlite.org/)
Oracle (http://www.oracle.com/)
MongoDb (https://django-mongodb-engine.readthedocs.org)
GoogleAppEngine Datastore (https://cloud.google.com/appengine/articles/django-nonrel)
You can refer to respective documentation to installing and configuring a database of your choice.

Note − Number 5 and 6 are NoSQL databases.

Step 4 – Web Server
Django comes with a lightweight web server for developing and testing applications. This server is pre-configured to work with Django, and more importantly, it restarts whenever you modify the code.

However, Django does support Apache and other popular web servers such as Lighttpd. We will discuss both the approaches in coming chapters while working with different examples.