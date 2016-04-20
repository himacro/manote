###########
Test
###########

*************
Inline Markup
*************

*text*

**text**

``text``

__text__

Hello\ **Text**\ Hello

:abbr:`LIFO(last-in, first-out)`

:command:`pacman -Syu`

:file:`/etc/pacman.conf`

:download:`Download<test.rst>`

:kbd:`C-x C-f`

:manpage:`ls(1)`

:menuselection:`Start --> Programs`

:program:`cmd`

:regexp:`\s{2,3}.*+`


*****
List
*****

* A
* B
* C

#. A
#. B
#. C

.. hlist::
    :columns: 3

    * A
    * B
    * C

* A
* B

  * B.1
  * B.2

* C

#. A
#. B

   #. B.1
   #. B.2

#. C

* A
* B

  #. B.1
  #. B.2

* C

#. A
#. B

   * B.1
   * B.2

#. C

*************
Source Code
*************
python code::

    import sys

    print("hello world")



.. highlight:: c

C code 1::

    #include <stdio.h>

    int main(int argc, const char *argv[])
    {
        printf('hello world!\n');
        return EXIT_SUCCESS;
    }

C code 2:

.. code-block:: c

    #include <stdio.h>

    int main(int argc, const char *argv[])
    {
        printf('hello world!\n');
        return EXIT_SUCCESS;
    }

*************
Domain
************

Stand Domain
============

.. option:: dest_dir

    Destination directory
