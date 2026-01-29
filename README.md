# CCL Introduction to Electronics course

## Table of Contents
> TODO: Add a table of contents

## Installation

### Prerequisites
CAT-SOOP depends on `python 3.11` or newer and `pip3` for installation. Additionally, the easiest way to download this course is using `git`.
Most systems should come with all of these pre-installed, and you can verify each with the following commands: 

```
python --version
pip3 --version
git --version
```

If the dependencies are not installed, you may use the following installation guide

<details>
<summary>Installing Prerequisites</summary>
To install `python`:

On Linux systems, install through your package manager, or [download and build from source](https://www.python.org/downloads/).

[Windows installation guide](https://docs.python.org/3/using/windows.html)

[MacOS installation guide](https://docs.python.org/3/using/mac.html)

When you install `python`, `pip` should automatically be installed.
If it isn't, then install `pip` using:

```
python -m ensurepip
```

To install `git`:

On Linux systems, install through your package manager.
Otherwise, [follow the installation guide for your OS](https://git-scm.com/install/).
</details>

### Installing CAT-SOOP
The [official documentation](https://catsoop.org/docs/installing/) is sufficient, but we'll summarise the process here nonetheless

<details>
<summary>Linux and MacOS</summary>

```
pip install catsoop
```

If the installation is successful, then you should get something similar to the following:

```
Successfully built catsoop
Installing collected packages: ply, mpmath, websockets, Unidecode, soupsieve, six, setuptools, pytokens, pyparsing, Pygments, pycparser, pluggy, platformdirs, pathspec, packaging, oauthlib, mypy_extensions, more-itertools, mistletoe, lxml, ldap3, iniconfig, filelock, click, pytest, jaraco.functools, httplib2, ecdsa, cffi, black, beautifulsoup4, python-jose, PyNaCl, oauth2, cheroot, bs4, PyLTI, catsoop
Successfully installed PyLTI-0.7.0 PyNaCl-1.6.0 Pygments-2.19.2 Unidecode-1.4.0 beautifulsoup4-4.13.5 black-25.9.0 bs4-0.0.2 catsoop-19.0.7 cffi-2.0.0 cheroot-11.0.0 click-8.3.0 ecdsa-0.19.1 filelock-3.19.1 httplib2-0.31.0 iniconfig-2.1.0 jaraco.functools-4.3.0 ldap3-2.9.1 lxml-6.0.2 mistletoe-1.4.0 more-itertools-10.8.0 mpmath-1.3.0 mypy_extensions-1.1.0 oauth2-1.9.0.post1 oauthlib-3.3.1 packaging-25.0 pathspec-0.12.1 platformdirs-4.4.0 pluggy-1.6.0 ply-3.11 pycparser-2.23 pyparsing-3.2.5 pytest-8.4.2 python-jose-3.5.0 pytokens-0.1.10 setuptools-80.9.0 six-1.17.0 soupsieve-2.8 websockets-12.0
```
</details>
<details>
<summary>Windows</summary>

```
pip install catsoop
```

If the installation is successful, then you should get something similar to the following:

```
Successfully built catsoop
Installing collected packages: ply, mpmath, websockets, Unidecode, soupsieve, six, setuptools, pytokens, pyparsing, Pygments, pycparser, pluggy, platformdirs, pathspec, packaging, oauthlib, mypy_extensions, more-itertools, mistletoe, lxml, ldap3, iniconfig, filelock, click, pytest, jaraco.functools, httplib2, ecdsa, cffi, black, beautifulsoup4, python-jose, PyNaCl, oauth2, cheroot, bs4, PyLTI, catsoop
Successfully installed PyLTI-0.7.0 PyNaCl-1.6.0 Pygments-2.19.2 Unidecode-1.4.0 beautifulsoup4-4.13.5 black-25.9.0 bs4-0.0.2 catsoop-19.0.7 cffi-2.0.0 cheroot-11.0.0 click-8.3.0 ecdsa-0.19.1 filelock-3.19.1 httplib2-0.31.0 iniconfig-2.1.0 jaraco.functools-4.3.0 ldap3-2.9.1 lxml-6.0.2 mistletoe-1.4.0 more-itertools-10.8.0 mpmath-1.3.0 mypy_extensions-1.1.0 oauth2-1.9.0.post1 oauthlib-3.3.1 packaging-25.0 pathspec-0.12.1 platformdirs-4.4.0 pluggy-1.6.0 ply-3.11 pycparser-2.23 pyparsing-3.2.5 pytest-8.4.2 python-jose-3.5.0 pytokens-0.1.10 setuptools-80.9.0 six-1.17.0 soupsieve-2.8 websockets-12.0
```

~This might not work because Microsoft breaks everything it touches~

> TODO: Make this much more concise, test the installation on Windows and troubleshoot the *actual* problems
> TODO: Merge the Windows installation guide with the Linux and MacOS installation guide, as they are nearly identical

If this doesn't work, [this document](https://docs.google.com/document/d/1sewvyJyMmb3SGvXOiBJl_tRL5CFrwiZbME2-a19OQGs) might help.
</details>

### Configuring CAT-SOOP

Once CAT-SOOP is installed, start the configuration with `catsoop configure`.
Typically, the defaults should be good enough.

The script asks the following questions:

> Are you setting up a production CAT-SOOP instance, or a local copy?
>
> [default: Local Copy]

Keep the default, unless you know what you're doing.

> Where should CAT-SOOP store its logs?
>
> [default: `~/.local/share/catsoop/` or `C:\Users\yourusername\.local\share\catsoop\`]

This is the director in which both the logs and the course content is stored.

> Which port should CAT-SOOP use for its web server?
>
> [default: 7667]

The port should be a number between 0 and 65535, although some of them might be used for other things, so it's recommended to keep the default.

> Which port should CAT-SOOP use for connections to the grader?
>
> [default: 7668]

This port must be different from the port for the web server.

> For courses that use "dummy" authentication, what username should be used?

This is the one question which does not have a default, so you must enter a value here. I used my name as the dummy username.

> Where should this configuration be saved?
>
> [default: `~/.config/catsoop/config.py` or `C:\Users\yourusername\.config\catsoop\config.py`]

This is where the configuration is stored. You can edit the configuration by either running `catsoop configure` or editing this file directly.

### Downloading and setting up the course

Navigate to the directory in which courses are stored (by default `~/.local/share/catsoop/courses` or `C:\Users\yourusername\.local\share\catsoop\`):

<details open>
<summary>Linux and MacOS</summary>

```
cd ~/.local/share/catsoop/courses
```

</details>
<details open>
<summary>Windows</summary>

```
cd C:\Users\yourusername\.local\share\catsoop\
```

</details>

Clone this repository:

```
git clone https://github.com/aaaarushi/ccl-electronics-course
```

If you want to store the course elsewhere, you can create a symbolic link pointing there instead.



## Running the course server locally

Run the CAT-SOOP server with `catsoop start` or `catsoop runserver` (the former is an alias for the latter).
Navigate to the server in a web browser. By default, this is at [http://localhost:7667](http://localhost:7667).
If you changed the port number, then use that instead.

