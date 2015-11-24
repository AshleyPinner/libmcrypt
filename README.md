# Libmcrypt

Libmcrypt is a thread-safe library providing a uniform interface
to access several block and stream encryption algorithms.

### This is going to be a project to upkeep libmcrypt

You may file issues in the issue tracker, and submit pull requests.
There will be an effort to clean up the code, and fix old issues.

All contributions welcome.



## Old notes:

Look at COPYING for license information and the individual files for more
information. COPYING applies only for the mcrypt program and not the
algorithms which most of them are public domain.


**
** Some hints:

Since 2.5.4 libmcrypt does not use dynamic loading for the modules by default.
All the algorithms and modes, are now included in the library. To enable
the old dynamic loading behaviour use the --enable-dynamic-loading in the
configure script.

That way you can statically link the library and be 100% thread safe,
since dlopen is not always thread safe.

You can also enable dynamic loading and include some algorithms into the
library. To include algorithms in the library use the
--with-included-algos parameter in the configure script.
Eg: ./configure --with-included-algos="rijndael-128 arcfour stream cbc cfb"


