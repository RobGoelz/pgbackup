pgbackup
========

CLI for backing up remote PostgreSQL databases locally or to AWS S3.

Preparing for Development
-------------------------

1. Ensure ``pip``, and ``pipenv`` are installed.
2. Clone the repository: ``git clone git@github.com/example/pgbackup``
3. Fetch development dependencies: ``make install``

Usage
-----

Pass in a ful database URL, the storage driver, and destination.

S3 Example with bucket name:

::

    $ pgbackup postgres://user@example.com:port/db_to_backup --driver s3 backups

Local Example w/ local path

::
    $ pgbackup postgres://user@example.com:port/db_to_backup --driver local /var/local/db_one/backups/dump.sql

Running Tests
-------------

Run tests locally using ``make`` if virtualenv is active:

::

    $ make

If virtualenv isn't active then use:

::

    $ pipenv run make
