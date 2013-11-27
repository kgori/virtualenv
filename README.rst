virtualenv
==========

.. image:: https://pypip.in/v/virtualenv/badge.png
        :target: https://pypi.python.org/pypi/virtualenv

.. image:: https://secure.travis-ci.org/pypa/virtualenv.png?branch=develop
   :target: http://travis-ci.org/pypa/virtualenv

For documentation, see http://www.virtualenv.org/

This fork of virtualenv automatically installs IPython into any new
environment unless ```--no-ipython``` is passed. 

Why did I want to add this trivial feature?
===========================================

There are a few packages I consider essential - Numpy, Scipy, Matplotlib,
Pandas - so I have them installed in my system python site-packages,
and I allow my virtualenvs to use them via the ```--system-site-packages```
flag. I would include IPython in the list of essentials, but there are
complications. IPython issues a warning if you try to use a system-wide
version inside a virtualenv, and it also makes the system python2 interpreter
inside a python3 venv, and vice versa. Maybe not a big deal, but to be avoided. 

So instead I want to install IPython into any new virtualenv. And the problem
is I forget. And this fork fixes that. 
