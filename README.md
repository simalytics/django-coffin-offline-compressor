django-coffin-offline-compressor
===============================

(c) Michael Chan, <michael@mchan.org>, 2013
License: MIT


To install
----------

First install it by:

```
pip install django-coffin-offline-compressor
```

To start with, this assumes that you have `django_compressor` and
`coffin` set up and working. 

Add `coffin_offline_compressor` to your `INSTALLED_APPS`.

To run
------

Just like you'd run regular `django_compressor` you now run:

```
./manage.py compress_coffin
```

And remember, unless you have `COMPRESS_OFFLINE = True` in your
settings you might have to do: 

```
./manage.py compress_coffin --force
```

That should now have created all the minified and concatenated files
in your `STATIC_ROOT` in a sub-directory called `CACHE`.   

**Note:** If you have other apps in `INSTALLED_APPS` that have been
added to `COFFIN_EXCLUDE_APPS` some of their templates might actually
be included in warnings when you run `compress_coffin`. Just ignore at
will.     

What's next
-----------

It's early days but hopefully if this stabilize and prove its
existence. Hopefully it can lead to a decent refactor and to have
tests so it can be patched upstream to `django_compressor`. Hint hint
@jezdez, keep an eye on me :)     


