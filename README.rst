
histfactory
===========

A script for common operations on HistFactory workspaces.

This script can:

* list the differences between two workspaces (including differences at the
  histogram level)
* fill empty background bins with the average sample weights
* rebin histograms
* merge specific bins in histograms
* smooth shape (HistoSys) systematics
* prune normalization (OverallSys) systematics
* prune shape (HistoSys) systematics by three separate methods (maximum
  deviation relative to total background statistical uncertainty, Chi2, and KS)

A new ROOT file and new set of XML files will be written out alongside the
input files with one or more of the above modifications.

Installation
------------

1. First setup at least Python 2.6 and ROOT 5.34 with PyROOT, XML,
   and RooFit enabled.

2. Download `rootpy <https://github.com/rootpy/rootpy>`_::

      git clone git://github.com/rootpy/rootpy.git

   or::

      svn checkout https://github.com/rootpy/rootpy/trunk rootpy

3. Then install rootpy::

      cd rootpy
      ./setup.py install --user

   See notes about setting up `rootpy on CERN's LXPLUS
   <https://github.com/rootpy/rootpy#try-rootpy-on-cerns-lxplus>`_ if you have
   trouble.


4. Download the script::

    curl -O https://raw.github.com/ndawe/histfactory/master/histfactory
    chmod +x histfactory

Usage
-----

Run the script on the top-level HistFactory XML file and from a directory where
the ROOT file containing the histograms is the same relative path as written in
the XML::

    ./histfactory path_to_my_xml/measurement.xml

See ``--help`` for more information::

    ./histfactory --help
