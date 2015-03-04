=======================
DEB build documentation
=======================

Prerequisites to build debs in general
--------------------------------------
 
Install build packages:

.. code-block:: bash

  sudo apt-get update
  sudo apt-get install dpkg-dev debhelper


Build deb for scrapyd
---------------------

To build a package for Ubuntu or Debian, you need to do it under the same kind of distribution so that upstart/sysinitv is chosen appropriately.

For instance for Debian:

.. code-block:: bash

  mkdir build-scrapy
  cd build-scrapy
  git clone -b medialab-debian https://github.com/medialab/scrapyd.git scrapyd
  cd scrapyd
  dpkg-buildpackage -us -uc
  

Collect the .deb package in the parent dir of scrapyd (build-scrapy in the above example).

