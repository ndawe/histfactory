
A script for common operations on HistFactory workspaces.

Download the script::

    curl -O https://raw.github.com/ndawe/histfactory/master/histfactory
    chmod +x histfactory

Run the script on the top-level HistFactory XML file and from a directory where
the ROOT file containing the histograms is the same relative path as written in
the XML::

    ./histfactory path_to_my_xml/measurement.xml

See the ``--help`` for more information::

    ./histfactory --help
