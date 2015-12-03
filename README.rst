Installing Python
=================

Mac OS X & Linux
----------------

0. Make sure you have ``gcc`` installed, e.g.::

    $ xcode-select --install  # OS X
    $ sudo apt-get install build-essential  # Debian, Ubuntu, Mint, etc.
    $ sudo yum group install "Development Tools"  # RedHat, CentOS

1. Install `pyenv <https://github.com/yyuu/pyenv>`_

    - If you're using `homebrew <https://github.com/homebrew/homebrew>`_ or
      `linuxbrew <https://github.com/Homebrew/linuxbrew>`_,
      follow the `homebrew installation instructions
      <https://github.com/yyuu/pyenv#homebrew-on-mac-os-x>`_
    - If you're not using homebrew, you probably should be
    - If you really insist on not using homebrew, follow the `basic
      installation instructions
      <https://github.com/yyuu/pyenv#basic-github-checkout>`_

2. Install the latest stable version of Python::

    $ pyenv install 3.5.0
    Downloading Python-3.5.0.tgz...
    -> https://yyuu.github.io/pythons/584e3d5a02692ca52fce505e68ecd77248a6f2c99adf9db144a39087336b0fe0
    Installing Python-3.5.0...
    Installed Python-3.5.0 to ~/.pyenv/versions/3.5.0

3. Set your global Python installation::

    $ pyenv global 3.5.0

Windows
-------

1. Download the installer from
   https://www.python.org/downloads/release/python-350/

    - 32 bit: https://www.python.org/ftp/python/3.5.0/python-3.5.0.exe
    - 64 bit: https://www.python.org/ftp/python/3.5.0/python-3.5.0-amd64.exe

2. Double click the installer to run it


Installing ``pip`` and creating your first virtual environment
==============================================================

All Platforms
-------------

0. Make sure ``python`` is in your path (usually not needed on OS X and Linux
   systems)::

    C:\>set PATH=C:\Program Files\Python 3.5;%PATH%  # Windows
    C:\>set PYTHONPATH=%PYTHONPATH%;C:\My_python_lib  # Windows

1. Make sure you have pip::

    $ python -m ensurepip
    Ignoring indexes: https://pypi.python.org/simple
    Requirement already satisfied (use --upgrade to upgrade): setuptools in ~/.pyenv/versions/3.5.0/lib/python3.5/site-packages
    Requirement already satisfied (use --upgrade to upgrade): pip in ~/.pyenv/versions/3.5.0/lib/python3.5/site-packages

2. Create a virtual environment (homework: check out `virtualenv
   <https://virtualenv.pypa.io/en/latest/>`_ and `virtualenvwrapper
   <https://virtualenvwrapper.readthedocs.org/en/latest/>`_)::

    $ pyvenv venv

3. Activate your virtual environment::

    $ source venv

4. Install a package::

    $ python -m pip install requests
    Collecting requests
    Using cached requests-2.8.1-py2.py3-none-any.whl
    Installing collected packages: requests
    Successfully installed requests-2.8.1

5. Verify that everything's working properly::

    $ python
    Python 3.5.0 (default, Dec  1 2015, 19:42:21)
    [GCC 4.2.1 Compatible Apple LLVM 7.0.0 (clang-700.1.76)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>> import requests
    >>> requests.__version__
    '2.8.1'

5. Embrace the Python philosophy::

    >>> import this
