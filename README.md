# GCI-Django-HelloWorld

A Django Hello World program for the GCI Fedora Project Task by Emmanuel Haankwenda.

Cloning the project
===================

    $ git clone https://github.com/emmanuel39hanks/GCI-Django-HelloWorld
    $ cd GCI-Django-HelloWorld

Installation
============

You need install the pre-requirements for run this Hello World example.
After cloning the project make sure you change directories into the cloned folder.
We will create a virtual environment.

Step 1 — Update and Upgrade

Logged into your Ubuntu 18.04 server as a sudo non-root user, first update and upgrade your system to ensure that your shipped version of Python 3 is up-to-date.


    $ sudo apt update
    $ sudo apt -y upgrade
  

Confirm installation if prompted to do so.

Step 2 — Check Version of Python
Check which version of Python 3 is installed by typing:


    $ python3 -V

  
You’ll receive output similar to the following, depending on when you have updated your system.

Output
Python 3.6.7
Step 3 — Install pip
To manage software packages for Python, install pip, a tool that will install and manage libraries or modules to use in your projects.


    $ sudo apt install -y python3-pip


Python packages can be installed by typing:


    $ pip3 install package_name


Here, package_name can refer to any Python package or library, such as Django for web development or NumPy for scientific computing. So if you would like to install NumPy, you can do so with the command pip3 install numpy.

Step 4 — Install Additional Tools
There are a few more packages and development tools to install to ensure that we have a robust set-up for our programming environment:


     $ sudo apt install build-essential libssl-dev libffi-dev python3-dev


Step 5 — Install venv
Virtual environments enable you to have an isolated space on your server for Python projects. We’ll use venv, part of the standard Python 3 library, which we can install by typing:


    $ sudo apt install -y python3-venv
  
  
Step 6 — Create a Virtual Environment
You can create a new environment with the pyvenv command. Here, we’ll call our new environment my_env, but you can call yours whatever you want.


    $ python3 -m venv my_env
  
  
Step 7 — Activate Virtual Environment
Activate the environment using the command below, where my_env is the name of your programming environment.


    $ source my_env/bin/activate


Step 8 - Install Django


    $ pip3 install django==2.2.0


First run:


    $ python3 manage.py migrate


At which point you should see:

::

    Operations to perform:
      Apply all migrations: admin, auth, contenttypes, sessions, sites
    Running migrations:

      Applying contenttypes.0001_initial... OK
      Applying auth.0001_initial... OK
      Applying admin.0001_initial... OK
      Applying admin.0002_logentry_remove_auto_add... OK
      Applying admin.0003_logentry_add_action_flag_choices... OK
      Applying contenttypes.0002_remove_content_type_name... OK
      Applying auth.0002_alter_permission_name_max_length... OK
      Applying auth.0003_alter_user_email_max_length... OK
      Applying auth.0004_alter_user_username_opts... OK
      Applying auth.0005_alter_user_last_login_null... OK
      Applying auth.0006_require_contenttypes_0002... OK
      Applying auth.0007_alter_validators_add_error_messages... OK
      Applying auth.0008_alter_user_username_max_length... OK
      Applying auth.0009_alter_user_last_name_max_length... OK
      Applying sessions.0001_initial... OK
      Applying sites.0001_initial... OK
      Applying sites.0002_alter_domain_unique... OK


For use the Django Admin Interface, it's needed to create a superuser 
for management, with the following command:



    $ python3 manage.py createsuperuser --username admin --email admin@mail.com

At which point you should see:



    Password:
    Password (again):

    Superuser created successfully.

Run application
===============

After which you can run:

    $ python3 manage.py runserver

Then, you can open the URL http://127.0.0.1:8000/ in your web browser and you can 
see the hello world:

Also you can open in your web browser the URL http://127.0.0.1:8000/admin for access to admin panel
