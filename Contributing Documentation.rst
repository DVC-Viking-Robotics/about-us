Basic Need-To-Know About Documentation
=======================================

What is Sphinx?
----------------

`Sphinx <http://www.sphinx-doc.org/en/master/>`_ is a third-party Python package that extends the builtin Python module `docutils <http://docutils.sourceforge.net/>`_. It can take the comment block in Python source code files and generate HTML pages for documentation purposes. In order to use Sphinx on your machine, you must install it via:

.. code-block:: shell

    pip install sphinx
    
or if you're running Linux:

.. code-block:: shell

    pip3 install sphinx

.. important:: All Sphinx-related files live in a repository's "./docs" folder.

All documentation is written in `reStructuredText syntax (rST for short) <http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#quick-syntax-overview>`_. This includes the comment blocks in the source code. Please refer to `this link <http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#quick-syntax-overview>`_ for more information on how to write in rST syntax (its not that hard, just a little different).

What is ReadTheDocs.org about?
------------------------------

ReadTheDocs.org (referred to as RTD) is a freely available domain hosting service that allows open source developers to host their software's documentation. Each software's documentation is represented by a "project" on RTD. RTD allows easy integration with version control services (like Github and Bitbucket). This means that, when properly set up, all changes pushed to a software's repository are automatically reflected on RTD (regarding the "./docs" folder). Each pushed commit from Github automatically triggers a new documentation build (this may take a couple minutes to complete on RTD's servers). You must install the RTD sphinx theme using

.. code-block:: shell

    pip install sphinx-rtd-theme
    
or if you're running Linux:

.. code-block:: shell

    pip3 install sphinx-rtd-theme

OK. Why does this matter?
-------------------------

If you've made changes to a repository's documentation (either in the source code or something in the "./docs" folder), then it is IMPRTANT that you check if the documentation can be built successfully. This is done locally BEFORE pushing a commit by running the following commands from the repository's root folder:

.. code-block:: shell
    
    cd docs
    sphinx-build -E -W . _build/HTML

If the build was successful, then you'll find a copy of the updated documentation pages in "./docs/_build/html". Open the "index.html" (or any html file) to load the documentation and make sure your changes appear as you expect them to. Once you have confirmed that the documentation changes are as they should be, then you are ready to push them onto the remote copy of the repository at Github. 

.. warning:: If you skip this step and the changes to the documentation are in error, then the entire build will fail on RTD and your changes will not take affect.

.. note:: you can delete the "_build/html" folder if you want. The repository should be setup to ignore this folder at all times, so that the test documentation pages aren't hogging up space on Github.
