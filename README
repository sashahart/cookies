What is this and what is it for?
--------------------------------

cookies.py is a Python module for working with HTTP cookies: parsing and
rendering both 'Cookie:' request headers, and 'Set-Cookie:' response headers,
and exposing a convenient API for creating and modifying cookies. It can be
used as a replacement of Python's Cookie.py (aka http.cookies). And it is just
one file under an MIT license, so you can drop it anywhere you want.

Its parsing is liberal, incorporating many complaints about Cookie.py, but it
tries to render strictly according to RFC 6265. It is designed to be customized
and extended and allow reuse of parts of the implementation without undue
difficulty. It is very well-documented, with chapter and verse from RFCs, and
has a more comprehensive test suite than Cookie.py. It is compatible with
Python 2.7, Python 3.x and PyPy.

Things this is not meant to do
------------------------------
While this is intended to be a good module for handling cookies, it does not
even try to do any of the following:

    * Maintain backward compatibility with Cookie.py, which would mean
      inheriting its confusions and bugs
    * Implement RFCs 2109 or 2965, which have always been ignored by almost
      everyone and are now obsolete as well
    * Handle every conceivable output from terrible legacy apps, which is not
      possible to do without lots of silent data loss and corruption (the
      parser does try to be liberal as possible otherwise, though)
    * Provide a means to store pickled Python objects in cookie values
      (that's a big security hole)

This doesn't compete with the cookielib module in the Python standard library,
which is specifically for implementing cookie storage and similar behavior in
an HTTP client such as a browser. Things cookielib does that this doesn't:

    * Write to or read from browsers' cookie stores or other proprietary
      formats for storing cookie data in files 
    * Handle the browser/client logic like deciding which cookies to send or
      discard, etc. 
