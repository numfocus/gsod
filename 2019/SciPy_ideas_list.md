# SciPy project ideas for GSoD'19

Welcome, and thank you for taking an interest in SciPy! On this page we will first provide some context about SciPy and the current state of its documentation, and then describe two project ideas in detail. We want to point out that we are not only interested in just these ideas; we'd love to talk to you if you have your own ideas about a project that you're excited about and that you think would help improve SciPy's documentation or online presence.

**About SciPy**: SciPy is *very* widely used in pretty much every field of science and engineering, and its uses base spans students who just learn to code to people doing state of the art scientific research and industrial R&D. SciPy is a core package of the scientific Python and PyData ecosystems. It provides a large collection of fundamental algorithms and data structures, from statistics and numerical optimization to linear algebra, Fourier transforms and sparse matrices. In some areas SciPy aims for comprehensive coverage (e.g. linear algebra, special functions), in others it provides key building blocks that are then built on by other project (e.g. [scikit-image](https://scikit-image.org/) provides much more complete coverage of image processing and builds on top of `scipy.ndimage`; [scikit-learn](https://scikit-learn.org) is the most well-known machine learning library in Python and builds on `scipy.sparse` and `scipy.linalg`).

**The state of SciPy's documentation**: SciPy has always been a volunteer project, and its documentation and websites reflect that fact. We have mostly complete reference documentation for each function and class exposed to users, although some functions are missing a usage example. We also have a tutorial per module, however most of these are not as complete as we would like and a few are missing. More importantly, the tutorial isn't laid out well for guiding users new to SciPy. Nor does it make any attempt to address *different kinds* of users. Improving the quality of SciPy documentation will be very valuable to our millions of users!

**How SciPy's documentation is built**: All our documentation and websites are built with [Sphinx](http://www.sphinx-doc.org). Sphinx generates static websites (so easy to deploy) and provides extensive functionality to transform plain-text *reStructuredText* documents to html, as well as extract and cross-link documentation automatically from docstrings in Python source code. Reference documentation follows the [NumPy docstring standard](https://numpydoc.readthedocs.io/en/latest/format.html). A detailed guide on how to document functions, classes and other objects can be found [here](https://www.numpy.org/devdocs/docs/howto_document.html), and how to build them [here](https://www.numpy.org/devdocs/docs/howto_build_docs.html) (note that the process for NumPy and SciPy is identical).

**SciPy's approach to documentation work**: Documentation tasks and issues are maintained on our [GitHub issue tracker](https://github.com/scipy/scipy/issues). Changes to the documentation are made via pull requests on GitHub, and reviewed with our standard review process which is the same for documentation and code (see our [contributing guide](http://scipy.github.io/devdocs/hacking.html)). For any new features added to SciPy, comprehensive reference documentation must be added at the same time as code, including usage examples. We do not have an overall "documentation work plan" to fix holes in existing documentation and restructure the documentation for, e.g., easier navigation. The core development team drives and decides on doc changes as they are proposed; there is no dedicated "documentation manager" (yet, our project maturity is still increasing! - see, e.g., our [developer guide](http://scipy.github.io/devdocs/hacking.html) and [governance structure](http://scipy.github.io/devdocs/dev/governance/governance.html)).


**Current documentation**:

- Latest version (tutorial, reference guide, developer docs): http://scipy.github.io/devdocs/
- Historical archive of released documentation: https://docs.scipy.org/doc/
- SciPy *ecosystem* website: https://scipy.org/
- SciPy *library* website: https://scipy.org/scipylib/index.html
- GitHub repository (all sources for code and docs): https://github.com/scipy/scipy/


## Contact

As a community driven project we try to have all conversations about SciPy in public. The main venue for discussions related to the *development* of SciPy (which includes GSoD) is the `scipy-dev` mailing list: https://scipy.org/scipylib/mailing-lists.html#mailing-lists. Please register and post to that list for discussing a GSoD proposal or idea. In case you want to pre-discuss something in private first, please contact the SciPy GSoD coordinators at numpy-scipy-gsod@googlegroups.com.


## Project idea: High level restructuring and end user focus

SciPy serves many kinds of users: students new to programming or Python, educators, researchers, domain experts in one of the areas that SciPy covers, data scientists, library developers, packagers, and more. And SciPy's documentation is *huge* (the pdf version of the last release is over 2500 pages). **The challenge**: *provide ways to guide those users to the parts of the documentation most relevant to them.* We would love to work with a technical writer that is able to help us address this challenge.

**Possible topics** include:
- Improving the structure and content of https://scipy.org/
- Reviewing and improving the structure of the main navigation page of [the SciPy documentation](http://scipy.github.io/devdocs/).
- Producing a roadmap or list of work items for engaging the community in further documentation work (we have a lot of contributor, channeling their energy by setting the right goals and priorities could have a lot of impact). This may include making explicit what different kinds of users need to see.
- Rewriting a section of the tutorial in a better style (that can then serve as a template for other/new sections).

We assume that the technical writer who will take on this project is not yet familiar with SciPy and its community. This means time will need to be built into the project plan at the start to get familiar with it. Mentors will be able to provide walkthroughs, set up time for discussing with or interviewing different kinds of end users, or anything else that in the writers experience is a good idea. *Note that some mentors have experience working with technical writers in a day-job-in-industry setting, but not in an open source setting - so we'll all learn a lot!*

**Relevant material** that is not yet linked above:

- The [SciPy Lecture Notes](https://scipy-lectures.org/), an external set of material specifically aimed at learning/teaching SciPy in courses.
- A [presentation at SciPy'18](https://www.youtube.com/watch?v=oHmm3mPxg6Y&t=797s) about SciPy's 1.0 release and its community.
- Another [SciPy tutorial](https://www.datacamp.com/community/tutorials/python-scipy-tutorial) and [cheat sheet](https://www.datacamp.com/community/blog/python-scipy-cheat-sheet).
- [Sources and executable notebooks](https://github.com/elegant-scipy/elegant-scipy) for the book [Elegant SciPy](https://www.ebooks.com/en-nl/95838978/elegant-scipy/nunez-iglesias-juan-walt-stefan-van-der-dashnow-ha/).
- The [goodreads list](https://www.goodreads.com/shelf/show/python-scipy) of books on "python-scipy". Many of those books are about the "SciPy ecosystem", which has NumPy and SciPy at its core.


## Project idea: Improving the documentation of scipy.stats

The aim of the project is to enhance the documentation of the statistics module of SciPy (`scipy.stats`). The current documentation contains a reference guide that describes the API of the functions and a tutorial (see *Related material* below for the links). The existing material can be extended in terms of content and quality.

Some ideas that a technical writer can work on:

* Improve the tutorial site of the stats module
    * review and suggest changes to improve the existing material
    * describe further use cases 
* Improve the documentation of the reference guide 
    * check whether current description can be improved, also taking into account known issues
    * add examples and references
    * cross-reference to other relevant / similar functions in the module

The second point would require good knowledge of statistics whereas the first point should only require basic knowledge. In general, the project leaves a lot of freedom to the technical writer depending on interest and background. The mentors would assist and provide guidance as needed.

This project would be suitable to a writer who wants to treat one submodule of SciPy in-depth. We hope to raise the quality of the documentation for this one module to a state-of-the-art level; that can then also serve as an example for other modules. Note that while `scipy.stats` is a good target as it is one of the most popular modules and an entry point for many students, we are also happy to discuss ideas for other modules with writers if they have specific interests.

**Related material**
* The [tutorial site](https://docs.scipy.org/doc/scipy/reference/tutorial/stats.html) of the stats module.
* The [reference guide of stats functions](https://docs.scipy.org/doc/scipy/reference/stats.html).
* An example of a function that only has a very brief documentation at the moment, [scipy.stats.zscore](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.zscore.html#scipy.stats.zscore).
* Examples of Github issues related to the documentation:
    * https://github.com/scipy/scipy/issues/9119 (missing docs)
    * https://github.com/scipy/scipy/issues/4952 (tutorial improvent suggestions by a user)
