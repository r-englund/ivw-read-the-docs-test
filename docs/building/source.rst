Getting the source
==================

Using git
~~~~~~~~~

Use git to clone the source code from GitHub_

.. _GitHub: http://www.github.com/inviwo/inviwo/

``git clone http://www.github.com/inviwo/inviwo.git``

Since we using the submodule feature of git for some of our external dependencies you need to make sure that submodules also has been cloned. Some applications, like SourceTree_, does this automatically. To clone/update all submodules run: 

.. _SourceTree: https://www.sourcetreeapp.com/

``git submodule update``


Downloading zip
~~~~~~~~~~~~~~~
Unfortunately GitHub does not include submodules when downloading source code from their webpage. Because of that, the only way of getting the source code at the moment is through using git. 