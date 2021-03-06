Cookiecutter Django
=======================

.. image:: https://requires.io/github/pydanny/cookiecutter-django/requirements.svg?branch=master
     :target: https://requires.io/github/pydanny/cookiecutter-django/requirements/?branch=master
     :alt: Requirements Status

.. image:: https://travis-ci.org/pydanny/cookiecutter-django.svg?branch=master
     :target: https://travis-ci.org/pydanny/cookiecutter-django?branch=master
     :alt: Build Status

.. image:: https://badges.gitter.im/Join Chat.svg
   :target: https://gitter.im/pydanny/cookiecutter-django?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge


A Cookiecutter_ template for Django.

.. _cookiecutter: https://github.com/audreyr/cookiecutter

Features
---------

* For Django 1.9
* Renders Django projects with 100% starting test coverage
* Twitter Bootstrap_ v4.0.0 - alpha_
* End-to-end via Hitch_
* AngularJS_
* 12-Factor_ based settings via django-environ_
* Optimized development and production settings
* Registration via django-allauth_
* Comes with custom user model ready to go.
* Grunt build for compass and livereload
* Basic e-mail configurations for sending emails via Mailgun_
* Media storage using Amazon S3
* Docker support using docker-compose_ for development and production
* Procfile_ for deploying to Heroku
* Works with Python 2.7.x or 3.5.x
* Run tests with unittest or py.test


Optional Integrations
---------------------

*These features can be enabled during initial project setup.*

* Serve static files from Amazon S3 or Whitenoise_
* Configuration for Celery_
* Integration with MailHog_ for local email testing
* Integration with Sentry_ for error logging
* Integration with NewRelic_ for performance monitoring
* Integration with Opbeat_ for performance monitoring

.. _alpha: http://blog.getbootstrap.com/2015/08/19/bootstrap-4-alpha/
.. _Hitch: https://github.com/hitchtest/hitchtest
.. _Bootstrap: https://github.com/twbs/bootstrap
.. _AngularJS: https://github.com/angular/angular.js
.. _django-environ: https://github.com/joke2k/django-environ
.. _12-Factor: http://12factor.net/
.. _django-allauth: https://github.com/pennersr/django-allauth
.. _django-avatar: https://github.com/jezdez/django-avatar/
.. _Procfile: https://devcenter.heroku.com/articles/procfile
.. _Mailgun: https://mailgun.com/
.. _Whitenoise: https://whitenoise.readthedocs.org/
.. _Celery: http://www.celeryproject.org/
.. _MailHog: https://github.com/mailhog/MailHog
.. _Sentry: https://getsentry.com
.. _NewRelic: https://newrelic.com
.. _docker-compose: https://www.github.com/docker/compose
.. _Opbeat: https://opbeat.com/


Constraints
-----------

* Only maintained 3rd party libraries are used.
* PostgreSQL everywhere (9.0+)
* Environment variables for configuration (This won't work with Apache/mod_wsgi).


Usage
------

Let's pretend you want to create a Django project called "redditclone". Rather than using `startproject`
and then editing the results to include your name, email, and various configuration issues that always get forgotten until the worst possible moment, get cookiecutter_ to do all the work.

First, get cookiecutter. Trust me, it's awesome::

    $ pip install cookiecutter

Now run it against this repo::

    $ cookiecutter https://github.com/pydanny/cookiecutter-django.git

You'll be prompted for some questions, answer them, then it will create a Django project for you.


**Warning**: After this point, change 'Daniel Greenfeld', 'pydanny', etc to your own information.

**Warning**: repo_name must be a valid Python module name or you will have issues on imports.

It prompts you for questions. Answer them::

    Cloning into 'cookiecutter-django'...
    remote: Counting objects: 550, done.
    remote: Compressing objects: 100% (310/310), done.
    remote: Total 550 (delta 283), reused 479 (delta 222)
    Receiving objects: 100% (550/550), 127.66 KiB | 58 KiB/s, done.
    Resolving deltas: 100% (283/283), done.
    project_name [project_name]: Reddit Clone
    repo_name [Reddit_Clone]: reddit
    author_name [Your Name]: Daniel Greenfeld
    email [Your email]: pydanny@gmail.com
    description [A short description of the project.]: A reddit clone.
    domain_name [example.com]: myreddit.com
    version [0.1.0]: 0.0.1
    timezone [UTC]:
    now [2016/03/01]: 2016/03/05
    year [2015]:
    use_whitenoise [y]: n
    use_celery [n]: y
    use_mailhog [n]: n
    use_sentry [n]: y
    use_newrelic [n]: y
    use_opbeat [n]: y
    use_pycharm [n]: y
    windows [n]: n
    use_python2 [n]: y
    Select open_source_license:
    1 - MIT
    2 - BSD
    3 - Not open source
    Choose from 1, 2, 3 [1]: 1

Enter the project and take a look around::

    $ cd reddit/
    $ ls

Create a GitHub repo and push it there::

    $ git init
    $ git add .
    $ git commit -m "first awesome commit"
    $ git remote add origin git@github.com:pydanny/redditclone.git
    $ git push -u origin master

Now take a look at your repo. Don't forget to carefully look at the generated README. Awesome, right?

For development, see the following for local development:

* `Developing locally`_
* `Developing locally using docker`_

.. _`Developing locally`: http://cookiecutter-django.readthedocs.org/en/latest/developing-locally.html
.. _`Developing locally using docker`: http://cookiecutter-django.readthedocs.org/en/latest/developing-locally-docker.html

For Readers of Two Scoops of Django 1.8
--------------------------------------------

You may notice that some elements of this project do not exactly match what we describe in chapter 3. The reason for that is this project, amongst other things, serves as a test bed for trying out new ideas and concepts. Sometimes they work, sometimes they don't, but the end result is that it won't necessarily match precisely what is described in the book I co-authored.

"Your Stuff"
-------------

Scattered throughout the Python and HTML of this project are places marked with "your stuff". This is where third-party libraries are to be integrated with your project.

Releases
--------

Want a stable release? You can find them at https://github.com/pydanny/cookiecutter-django/releases


Not Exactly What You Want?
---------------------------

This is what I want. *It might not be what you want.* Don't worry, you have options:

Fork This
~~~~~~~~~~

If you have differences in your preferred setup, I encourage you to fork this to create your own version.
Once you have your fork working, let me know and I'll add it to a '*Similar Cookiecutter Templates*' list here.
It's up to you whether or not to rename your fork.

If you do rename your fork, I encourage you to submit it to the following places:

* cookiecutter_ so it gets listed in the README as a template.
* The cookiecutter grid_ on Django Packages.

.. _cookiecutter: https://github.com/audreyr/cookiecutter
.. _grid: https://www.djangopackages.com/grids/g/cookiecutters/

Or Submit a Pull Request
~~~~~~~~~~~~~~~~~~~~~~~~~

We also accept pull requests on this, if they're small, atomic, and if they make our own project development
experience better.

Articles
---------

* `Development and Deployment of Cookiecutter-Django on Fedora`_ - Jan. 18, 2016
* `Development and Deployment of Cookiecutter-Django via Docker`_ - Dec. 29, 2015
* `How to create a Django Application using Cookiecutter and Django 1.8`_ - Sept. 12, 2015

Got a blog or online publication? Write about your cookiecutter-django tips and tricks, then send us a pull request with the link.

.. _`Development and Deployment of Cookiecutter-Django via Docker`: https://realpython.com/blog/python/development-and-deployment-of-cookiecutter-django-via-docker
.. _`Development and Deployment of Cookiecutter-Django on Fedora`: https://realpython.com/blog/python/development-and-deployment-of-cookiecutter-django-on-fedora/
.. _`How to create a Django Application using Cookiecutter and Django 1.8`: http://blog.swapps.co/how-to-create-a-django-application-using-cookiecutter-and-django-1-8/#.VxKfBpMrKRs

Support This Project
---------------------------

This project is maintained by volunteers. Support their efforts by spreading the word about:

.. image:: https://s3.amazonaws.com/tsacademy/images/tsa-logo-250x60-transparent-01.png
   :name: Two Scoops Academy
   :align: center
   :alt: Two Scoops Academy
   :target: http://www.twoscoops.academy/
