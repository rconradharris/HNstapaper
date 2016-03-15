==========
HNstapaper
==========

Automatically add HN articles to Instapaper.

By default, HNstapaper automatically selects articles that are over 1000 words
in length and have a minimum HN score of 200. These values are configurable on
the command line with the `-s` and `-w` options respectively.

The first run of HNstapaper will take a long time since it has to remotely
fetch the data for 500 stories.  Subsequent runs will be much faster since
this data will be available locally.


Install It
==========

pip install -r requires.txt


Run It
======

./HNstapaper -u <YOUR-INSTAPAPER-USERNAME> -p <YOUR-INSTAPAPER-PASSWORD> -v


Automate It
===========

You can cron this up to run everyday at 9:00 by adding the following lines to
your `crontab`::

    0 9 * * * /usr/local/bin/HNstapaper -u <YOUR-INSTAPAPER-USERNAME> -p <YOUR-INSTAPAPER-PASSWORD> -v

Requires
========

* requests
* goose-extractor
