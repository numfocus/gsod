# SciPy project ideas for GSoD'19

Welcome, and thank you for taking an interest in SciPy! On this page we will first provide some context about SciPy and the current state of its documentation, and then describe two project ideas in detail. We want to point out that we are not only interested in just these ideas; we'd love to talk to you if you have your own ideas about a project that you're excited about and that you think would help improve SciPy's documentation or online presence.

**About SciPy**: SciPy is *very* widely used in pretty much every field of science and engineering, and its uses base spans students who just learn to code to people doing state of the art scientific research and industrial R&D. SciPy is a core package of the scientific Python and PyData ecosystems. It provides a large collection of fundamental algorithms and data structures, from statistics and numerical optimization to linear algebra, Fourier transforms and sparse matrices. In some areas SciPy aims for comprehensive coverage (e.g. linear algebra, special functions), in others it provides key building blocks that are then built on by other project (e.g. [scikit-image](https://scikit-image.org/) provides much more complete coverage of image processing and builds on top of `scipy.ndimage`; [scikit-learn](https://scikit-learn.org) is the most well-known machine learning library in Python and builds on `scipy.sparse` and `scipy.linalg`).

**The state of SciPy's documentation**: SciPy has always been a volunteer project, and its documentation and websites reflect that fact. We have mostly complete reference documentation for each function and class exposed to users, although some functions are missing a usage example. We also have a tutorial per module, however most of these are not as complete as we would like and a few are missing. More importantly, the tutorial isn't laid out well for guiding users new to SciPy. Nor does it make any attempt to address *different kinds* of users. Improving the quality of SciPy documentation will be very valuable to our millions of users!

**How SciPy's documentation is built**: All our documentation and websites are built with [Sphinx](http://www.sphinx-doc.org). Sphinx generates static websites (so easy to deploy) and provides extensive functionality to transform plain-text *reStructuredText* documents to html, as well as extract and cross-link documentation automatically from docstrings in Python source code. Reference documentation follows the [NumPy docstring standard](https://numpydoc.readthedocs.io/en/latest/format.html). A detailed guide on how to document functions, classes and other objects can be found [here](https://www.numpy.org/devdocs/docs/howto_document.html), and how to build them [here](https://www.numpy.org/devdocs/docs/howto_build_docs.html) (note that the process for NumPy and SciPy is identical).

**Current documentation**:

- Latest version (tutorial, reference guide, developer docs): http://scipy.github.io/devdocs/
- Historical archive of released documentation: https://docs.scipy.org/doc/
- SciPy *ecosystem* website: https://scipy.org/
- SciPy *library* website: https://scipy.org/scipylib/index.html
- GitHub repository (all sources for code and docs): https://github.com/scipy/scipy/


## Contact

As a community driven project we try to have all conversations about SciPy in public. The main venue for discussions related to the *development* of SciPy (which includes GSoD) is the `scipy-dev` mailing list: https://scipy.org/scipylib/mailing-lists.html#mailing-lists. Please register and post to that list for discussing a GSoD proposal or idea. In case you really want to pre-discuss something in private first, please contact the SciPy GSoD coordinator (Ralf Gommers, ralf.gommers@gmail.com).




## Project: Improving the documentation of scipy.stats

The aim of the project is to enhance the documentation of the statistics module of SciPy (scipy.stats). The current documentation contains a reference guide that describes the API of the functions and a tutorial (see *Related material* below for the links). The existing material can be extended in terms of content and quality. 

Some ideas that a technical writer can work on:

* improve the tutorial site of the stats module
    * review and suggest changes to improve the existing material
    * describe further use cases 
* improve the documentation of the reference guide 
    * check whether current description can be improved, also taking into account known issues
    * add examples and references
    * cross-reference to other relevant / similar functions in the module

The second point would require good knowledge of statistics whereas the first point should only require basic knowledge. In general, the project leaves a lot of freedom to the technical writer depending on interest and background. The mentors would assist and provide guidance as needed.

**Related material**
* tutorial site of the stats module: https://docs.scipy.org/doc/scipy/reference/tutorial/stats.html
* reference guide of stats functions https://docs.scipy.org/doc/scipy/reference/stats.html
* example of a function that only has a very brief documentation at the moment https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.zscore.html#scipy.stats.zscore
* example of Github issues related to the documentation:
    * https://github.com/scipy/scipy/issues/9119
    * https://github.com/scipy/scipy/issues/4952
