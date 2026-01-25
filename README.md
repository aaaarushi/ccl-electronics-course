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