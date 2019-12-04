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


    $ sudo apt update
    $ sudo apt -y upgrade


Step 2 — Install pip
To manage software packages for Python, install pip, a tool that will install and manage libraries or modules to use in your projects.


    $ sudo apt install -y python3-pip


Step 4 — Install Additional Tools


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



Running the app
===============

    $ python3 manage.py runserver

To access the app visit the URL  http://127.0.0.1:8000/ in your browser, You should see the 'Hello World'
