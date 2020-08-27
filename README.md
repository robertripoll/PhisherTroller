PhisherTroller: Tool to troll phishers with fake data
=======================================

This tool is intended to be used in phishing websites, where credentials are stolen from the users by showing a replica of the original website.

**DISCLAIMER:** I am NOT responsible for any misuse or damage caused by this program. Use this tool at your own risk and under your responsibility!

What is PhisherTroller?
-------------

PhisherTroller is a *Python* tool to POST fake data (generated with *Faker*) to a phishing website, in order to confuse the phisher.

Here is a small example to troll a phisher:

```console
foo@bar:~$ python3 troller.py -u http://phishing-url.com/post.php -fu username -fp password
```

Requirements
------------

You need Python 3 to run PhisherTroller, as well as the following PIP dependencies:

* requests
* urllib3
* Faker

Setup
-----------

Clone the repository:

```console
foo@bar:~$ git clone https://github.com/UngarMax/PhisherTroller.git
```

Access the cloned repository directory:

```console
foo@bar:~$ cd PhisherTroller
```

Install the required dependencies:

```console
foo@bar:~$ pip install -r requirements.txt
```

Profit!

Guide
-----------

1. Go to the phishing website and open Chrome's Developer Tools.
2. Find out the username/email input's name.
3. Find out the password input's name.
4. Find out the form's action path.
5. Execute the trolling tool passing the form action path, username input name and password input name (and specify a miliseconds delay between each request, if you will):

```console
foo@bar:~$ python3 troller.py -u http://phishing-url.com/path/to/post.php -fu username_input_name -fp password_input_name -d 1000
```

Profit!

Usage
-----------

```
Usage: phisher_destroyer.py [-h] -u URL -fu FORM_USER -fp FORM_PASSWORD
                            [-d DELAY]

Arguments:
  -h, --help            show this help message and exit
  -u URL, --url URL     URL to POST fake data
  -fu FORM_USER, --form-user FORM_USER
                        Form input's name for username or email field
  -fp FORM_PASSWORD, --form-password FORM_PASSWORD
                        Form input's name for password field
  -d DELAY, --delay DELAY
                        Delay between each request, in miliseconds
```

License
-------

PhisherTroller is licensed under the terms of the MIT License (see the file LICENSE).
