==========================
 Debug mode
==========================

.. admonition:: Description

    Plone can be put in the debug mode where changes to CSS, Javascript
    and page templates take effect immediately.

Introduction
===============

By default when you start Plone you start it in a *production mode*.

* Plone is fast

* CSS and Javascript files are merged instead of causing multipe HTTP request to load these assets

* Plone does not reload changed filed on the disk

But because of above optimizations the development against a production mode is not feasible.
Instead you need to start Plone in debug mode (also known as development mode) if you
are doing any site development.


On Microsoft Windows
==============================

This document explains how to start and run the latest Plone (Plone 4.1.4) on Windows 7. This document explains post-installer steps on how to start and enter into a Plone site.
Installation

Installation
------------
This quick start has been tested on Windows 7.  Installation remains the same on older versions of Windows through WinXP.

1. Run installer from `Plone.org <http://plone.org/products>`_ download page

2. The Plone buildout directory will be installed in C:\\Plone41

3. The installer will launch your Plone instance when it finishes.  To connect, direct your browser to: http://127.0.0.1:8080

.. note::
   In the buildout bin directory you'll find the executable files to control Plone instance.

For greater insight into the Windows installation process, `Plone 4 Windows Installer Notes <http://plone.org/documentation/kb/plone-4-windows-installer>`_ provides alternate deployment strategies for Windows.

Starting and Stopping Plone
---------------------------

If your Plone instance is shutdown you can start and control it from the command prompt.

.. note::
   To control Plone you need to execute your command prompt as an administrator.

In the command prompt enter the following command to access your buildout directory
(the varies according to Plone version)::


   cd "C:\\Plone41"

To start Plone in debug mode type::

   bin\instance fg

You can interrupt the instance by pressing CTRL-C. This will also take down the Zope application server and your Plone site.

Accessing Plone
---------------

When you launch Plone in debug or daemon mode it will take a few moments to launch.  If you are in debug mode, Plone will be ready serve pages when the following line is displayed in your command prompt::

   INFO Zope Ready to handle requests

When the instance is running and listing to port 8080, point your browser to address on your local computer::

   http://127.0.0.1:8080

The Plone welcome screen will load and you can create your first Plone site directly by clicking the **Create a new Plone Site** button.

A form will load asking for the *Path Identifier* (aka the site id) and *Title* for a new Plone site.  It will also allow you to select the main site language, and select any add-on products you wish to install with the site.

.. note::
   These entries can all be modified once the site is created.  Changing the site id is possible, but not recommended.

To create your site, fill in this form and click the *Create Plone Site* button.  Plone will then create and load your site.

.. note::
   The url of your local Plone instance will end with the site id you set when setting up your site.  If the site id were *Plone* then the resultant URL is: *http://127.0.0.1:8080/Plone*.

Congratulations! You should be now logged in as an admin to your new Plone instance and you'll see the front page of Plone.


On Unix
==============================

Enter to your installation folder using `cd` command (depends on where you have installed Plone).

Type in command::

    bin/instance fg

Press CTRL+C to stop.




