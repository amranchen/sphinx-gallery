Change Log
==========

git master
----------

Developer changes
'''''''''''''''''
* Support on the fly theme change for local builds of the
  Sphinx-Gallery docs. Passing to the make target the variable `theme`
  builds the docs with the new theme. All sphinx themes are available
  plus read the docs online theme under the value `rtd` as shown in this
  usage example.::

    $ make html theme=rtd


v0.1.4
------

New features
''''''''''''
* Enhanced CSS for download buttons
* Download buttons at the end of the gallery to download all python
  scripts or Jupyter notebooks together in a zip file. New config
  variable `download_all_examples` to toggle this effect. Activated by
  default
* Downloadable zip file with all examples as Python scripts and
  notebooks for each gallery
* Improved conversion of rst directives to markdown for the Jupyter
  notebook text blocks

Bug Fixes
'''''''''
* When seaborn is imported in a example the plot style preferences are
  transferred to plots executed afterwards. The CI is set up such that
  users can follow how to get the compatible versions of
  mayavi-pandas-seaborn and nomkl in a conda environment to have all
  the features available.
* Fix math conversion from example rst to Jupyter notebook text for
  inline math and multi-line equations

v0.1.3
------

New features
''''''''''''
* Summary of failing examples with traceback at the end of the sphinx
  build. By default the build exits with a 1 exit code if an example
  has failed. A list of examples that are expected to fail can be
  defined in `conf.py` and exit the build with 0
  exit code. Alternatively it is possible to exit the build as soon as
  one example has failed.
* Print aggregated and sorted list of computation times of all examples
  in the console during the build.
* For examples that create multiple figures, set the thumbnail image.
* The ``plot_gallery`` and ``abort_on_example_error`` options can now
  be specified in ``sphinx_gallery_conf``. The build option (``-D``
  flag passed to ``sphinx-build``) takes precedence over the
  ``sphinx_gallery_conf`` option.

Bug Fixes
'''''''''

* Failing examples are retried on every build


v0.1.2
------

Bug Fixes
'''''''''

* Examples that use ``if __name__ == '__main__'`` guards are now run
* Added vertical space between code output and code source in non
  notebook examples

v0.1.1
------

Bug Fixes
'''''''''

* Restore the html-noplot functionality
* Gallery CSS now implicitly enforces thumbnails width

v0.1.0
------

Highlights
''''''''''

Example scripts are now available for download as IPython Notebooks
`#75 <https://github.com/sphinx-gallery/sphinx-gallery/pull/75>`_

New features
''''''''''''

* Configurable filename pattern to select which example scripts are
  executed while building the Gallery
* Examples script update check are now by md5sum check and not date
* Broken Examples now display a Broken thumbnail in the gallery view,
  inside the rendered example traceback is printed. User can also set
  build process to abort as soon as an example fails.
* Sorting examples by script size
* Improve examples style

v0.0.11
-------

Highlights
''''''''''

This release incorporates the Notebook styled examples for the gallery
with PR `#36
<https://github.com/sphinx-gallery/sphinx-gallery/pull/36>`_

Incompatible Changes
''''''''''''''''''''

Sphinx-Gallery renames its python module name to sphinx\_gallery this
follows the discussion raised in `#47
<https://github.com/sphinx-gallery/sphinx-gallery/issues/47>`_ and
resolved with `#66
<https://github.com/sphinx-gallery/sphinx-gallery/pull/66>`_

The gallery configuration dictionary also changes its name to ``sphinx_gallery_conf``

From PR `#36
<https://github.com/sphinx-gallery/sphinx-gallery/pull/36>`_ it is
decided into a new namespace convention for images, thumbnails and
references. See `comment
<https://github.com/sphinx-gallery/sphinx-gallery/pull/36#issuecomment-121392815>`_


v0.0.10
-------

Highlights
''''''''''

This release allows to use the Back references. This features
incorporates fine grained examples galleries listing examples using a
particular function. `#26
<https://github.com/sphinx-gallery/sphinx-gallery/pull/26>`_

New features
''''''''''''

* Shell script to place a local copy of Sphinx-Gallery in your project
* Support Mayavi plots in the gallery
