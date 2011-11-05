What this is
------------

cookies.py is a Python module for working with HTTP cookies: parsing and
rendering both 'Cookie:' request headers, and 'Set-Cookie:' response headers,
and exposing a convenient API for creating and modifying cookies. It can be
used as a replacement of Python's Cookie.py (aka http.cookies).

Its parsing is liberal, incorporating many complaints about Cookie.py, but it
tries to render strictly according to RFC 6265. It is designed to be customized
and extended and allow reuse of parts of the implementation without undue
difficulty. It is very well-documented, with chapter and verse from RFCs, and
has a more comprehensive test suite than Cookie.py. It is compatible with
Python 3 and PyPy.

What it doesn't do
------------------

    * Maintain backward compatibility with Cookie.py
    * Implement RFCs 2109 or 2965, which are obsolete and almost universally ignored
    * Handle every conceivable output from terrible PHP or Java apps
    * Provide a means to store pickled Python objects in cookie values (security hole)
    * Write to or read from browsers' cookie stores
    * Handle the client logic of deciding which cookies to send or discard 
