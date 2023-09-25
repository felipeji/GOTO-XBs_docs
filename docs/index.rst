.. GOTO-XBs documentation master file, created by
   sphinx-quickstart on Thu Sep 21 11:05:15 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to GOTO-XBs' documentation!
====================================

GOTO-XBs is a web platform for follow-up of X-ray binaries (XBs) within GOTO data. It provides access to light curves for all known X-ray binaries, constructed from all the observed epochs and across the 4 GOTO bands. The object database can be updated with newly discovered X-ray binaries, triggering the automatic generation of historical light curves for these objects.

The platform also features a range of analysis tools for working with light curves in real-time. These tools include data filtering, phase folding,  smoothing within user-defined time windows, periodogram analysis, plot generation, and more.

Users can download the data, both raw or previously filtered or/and smoothed light curves.


The platform is built on a Django framework. So far it consists of two applications:

- **dashboard**: a list of the sources being followed. They are organized in a table that makes it easy to find them.

- **source_viewer**:  produces an individual webpage for each object with its information. It use ``plotly`` for creating an interactive plot of the object light curve in GOTO and it allows to download the data.





Contents
--------

.. toctree::
   :maxdepth: 2

   requirements
   quick_start
   databases

