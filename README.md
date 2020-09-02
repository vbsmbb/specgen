# specgen

This is a direct port of Bo Ferris and Sergio Fernandez specgen repository. They called their version specgen6 which was an update of Dan Brickley's specgen5 repository. Their repository was based on using python2 on a Unix/Linux host. I ported the code to python3 (3.8.5) on a Windows platform. 

The worst problem found was sporadioc spacing which caused havoc in the Windows python 3.8.5 version. The worst module was libvocab.py. The problem Since the version that I ported from had not been updated in about eight years, there were a few things that had to be changed and at least one still needs updating. I made no changes to how things should work or tried to update the logic in any way. I ported only to the point of getting the sample command to work in the windows python environment.

I added a new requirements.txt file becuase the number of modules required to make this work in the windows environment was very different from the one downloaded. I started with a new clean virtual environment with nothing but pip, setuptools, and wheel. Then I added the four modules (rdflib, rdfextras, pyparsing, and python-igraph), using pip, from the original requirments file one at a time and allowed them to add all of their dependencies. That is how the list grew to it's existing twenty modules.

This works with the command from the example in the Ferris/Hernandez repository. This command is included in the file named, specgen7.cmd. This command works from the wiondows command line and creates the expected files. The example files and directories are as they were in the specgen/specgen repository.
