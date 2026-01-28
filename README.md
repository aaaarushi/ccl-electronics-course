# CCL Intro to Electronics Course on CATSOOP

This document details how to get a course website running locally

FOR WINDOWS INSTALL refer to this document: https://docs.google.com/document/d/1sewvyJyMmb3SGvXOiBJl_tRL5CFrwiZbME2-a19OQGs/edit?tab=t.0

For CATSOOP official installation docs: https://catsoop.org/docs/installing

## Install

1. Install Python 3.12 from the official Python page: https://www.python.org/downloads/release/python-3120/

    Open the exe file click install python.exe in path

    open terminal application

    `python --version`
    `pip --version`

2. `pip install catsoop`

3. `catsoop configure`

> NOTE FOR WINDOWS:

>    You might get an error "libc not found"

>    Run `pip show catsoop`

>    This shows which file path catsoop is installed in, should be something like this C:\Users\tejor\AppData\Local\Programs\Python\Python312\Lib\site-packages\catsoop

>    Go to that path - you can use the file explorer, start from your C:// drive and go until the catsoop folder

>    Now you will need to change some of the files in the catsoop library, see the above Windows installation document for reference

4. Install git from the souce page: https://github.com/git-guides/install-git

    All defaults are fine

TODO: explain how to use git and set up ssh keys so you can clone this repo with ssh, explain how to open up files in vscode

## Install on MacOS

First, check `python` and `pip` versions

    `python --version`
    `pip --version`

On my machine (with MacOS 26.2), these are the versions of both

``
python --version
Python 3.12.10

pip --version
pip 25.2 from /Library/Frameworks/Python.framework/Versions/3.12/lib/python3.12/site-packages/pip (python 3.12)
``

Next, install `catsoop`

`pip install catsoop`

If it works, you should see something like below on your terminal

``
Successfully built catsoop
Installing collected packages: ply, mpmath, websockets, Unidecode, soupsieve, six, setuptools, pytokens, pyparsing, Pygments, pycparser, pluggy, platformdirs, pathspec, packaging, oauthlib, mypy_extensions, more-itertools, mistletoe, lxml, ldap3, iniconfig, filelock, click, pytest, jaraco.functools, httplib2, ecdsa, cffi, black, beautifulsoup4, python-jose, PyNaCl, oauth2, cheroot, bs4, PyLTI, catsoop
Successfully installed PyLTI-0.7.0 PyNaCl-1.6.0 Pygments-2.19.2 Unidecode-1.4.0 beautifulsoup4-4.13.5 black-25.9.0 bs4-0.0.2 catsoop-19.0.7 cffi-2.0.0 cheroot-11.0.0 click-8.3.0 ecdsa-0.19.1 filelock-3.19.1 httplib2-0.31.0 iniconfig-2.1.0 jaraco.functools-4.3.0 ldap3-2.9.1 lxml-6.0.2 mistletoe-1.4.0 more-itertools-10.8.0 mpmath-1.3.0 mypy_extensions-1.1.0 oauth2-1.9.0.post1 oauthlib-3.3.1 packaging-25.0 pathspec-0.12.1 platformdirs-4.4.0 pluggy-1.6.0 ply-3.11 pycparser-2.23 pyparsing-3.2.5 pytest-8.4.2 python-jose-3.5.0 pytokens-0.1.10 setuptools-80.9.0 six-1.17.0 soupsieve-2.8 websockets-12.0
``


NOTE: there is a chance that even after the installation is successful, you will not be able to run 
`catsoop` from the same shell that you installed the application from. If this happens, open a new 
shell and it should work.

## Configure on MacOS

Start the configuration command for `catsoop`

 `catsoop configure`

 When presented with options, choose `Local Copy`.

Next, choose the default location for storing logs (`$HOME/.local/share/catsoop`)

NOTE: this is the directory where any new courses that you start will also be located, so it is 
advised to leave it as the default value.

Keep the default port for the application (7667).

Keep the default port for `catsoop` to listen for connections on (7668).

Enter a known username for the dummy authenticated user. I used `manuawasthi`. 

Save the configuration at the default location prompted by `catsoop`. In my case it was `$HOME/.config/catsoop/config.py`

Hit `Enter` on the confirmation prompt. 

Once this is done, you should be ready to start `catsoop` using `catsoop start`.

The following assumes that you have access to the [course repository](https://github.com/aaaarushi/ccl-electronics-course). Otherwise, try the commands with the orginal [catsoop repo on github](https://catsoop.org/git/catsoop/catsoop).


### Setup the CCL Course
`cd $HOME/.local/share/catsoop/courses`

`git clone git@github.com:aaaarushi/ccl-electronics-course.git`


Once this is done, do `catsoop start` from the terminal. Then, go to `http://localhost:7667` in your
browser, and you should be able to see the list of courses (in this case `ccl-electronics-course: Introduction to Electronics` at the bottom). 

Alternatively, you can directly access the electronics course at this URL `http://localhost:7667/ccl-electronics-course`







