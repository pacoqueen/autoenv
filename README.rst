Autoenv: Directory-based Environments
======================================

Magic per-project shell environments. Very pretentious.


What is it?
-----------

If a directory contains a ``pyvenv.cfg`` file, it will automatically activate
when you ``cd`` into it. It will deactivate it if you ``cd ..``.

Usage
-----

Follow the white rabbit::

    $ pyvenv my-fancy-project
    $ cd my-fancy-project

.. image:: http://media.tumblr.com/tumblr_ltuzjvbQ6L1qzgpx9.gif


Install
-------

Install it easily. It works with zsh too. Change ``.bashrc`` with ``.zshenv``:

Mac OS X Using Homebrew
~~~~~~~~~~~~~~~~~~~~~~~

::

    $ brew install autoenv
    $ echo 'source /usr/local/opt/autoenv/activate.sh' >> ~/.bash_profile


Using pip
~~~~~~~~~

::

    $ pip install autoenv
    $ echo "source `which activate.sh`" >> ~/.bashrc


Using git
~~~~~~~~~

::

    $ git clone git://github.com/kennethreitz/autoenv.git ~/.autoenv
    $ echo 'source ~/.autoenv/activate.sh' >> ~/.bashrc


Disclaimer
----------

Autoenv overrides ``cd``. If you already do this, invoke ``autoenv_init`` within your custom ``cd`` after sourcing ``activate.sh``.

Autoenv can be disabled via ``unset cd`` if you experience I/O issues with
certain file systems, particularly those that are FUSE-based (such as 
``smbnetfs``).

Testing
-------

Install the test runner::

    $ make
    gem install dtf --version 0.1.2
    Successfully installed dtf-0.1.2

Test::

    $ make test
    dtf tests/*
    ............
    ##### Processed commands 14 of 14, success tests 12 of 12.
