# NumPy project ideas for GSoD'19

Welcome, and thank you for taking an interest in NumPy! On this page we will
first provide some context about NumPy and the current state of its
documentation, and then describe one project idea in detail. We want to point
out that we are not only interested in just that idea; we'd love to talk to you
if you have your own ideas about a project that you're excited about and that
you think would help improve NumPy's documentation or online presence.

**About NumPy**: NumPy is *very* widely used in pretty much every field of
science and engineering. Its user base spans from beginning coders to
experienced researchers doing state-of-the-art scientific and industrial R&D.
NumPy is the *universal standard* for working with numerical data in Python,
and at the core of the scientific Python and PyData ecosystems. It provides
`ndarray`, a homogeneous n-dimensional array object with methods to efficiently
operate on it. The NumPy API is used extensively in Pandas, SciPy, Matplotlib,
scikit-learn, scikit-image and most other data science and scientific Python
package. The API and concepts are also replicated in deep learning frameworks
(e.g.  Tensorflow, PyTorch) and in array computing libraries for other
programming languages.

**The state of NumPy's documentation**: NumPy has been a 100% volunteer project
until the first half of 2018 (we now have 2 full-time paid developers), and its
documentation and websites reflect that fact. We have mostly complete reference
documentation for each function and class exposed to users, although some
functions are missing a usage example. We also have a User Guide, however it is
not in very good shape. The User Guide and website (https://numpy.org) are not
laid out well for guiding users new to NumPy. Nor do they make any attempt to
address *different kinds* of users. Improving the quality of NumPy
documentation will be very valuable to our millions of users!

**How NumPy's documentation is built**: All our documentation and websites are
built with [Sphinx](http://www.sphinx-doc.org). Sphinx generates static
websites (making them easy to deploy) and provides extensive functionality to
transform plain-text *reStructuredText* documents to html, as well as extract
and cross-link documentation automatically from docstrings in Python source
code.  Reference documentation follows the [NumPy docstring standard]
(https://numpydoc.readthedocs.io/en/latest/format.html). A detailed
guide on how to document functions, classes and other objects can be found
[here](https://www.numpy.org/devdocs/docs/howto_document.html), and how to
build them [here](https://www.numpy.org/devdocs/docs/howto_build_docs.html).

**NumPy's approach to documentation work**: Documentation tasks and issues are
maintained on our [GitHub issue tracker](https://github.com/numpy/numpy/issues).
Changes to the documentation are made via pull requests on GitHub, and reviewed
with our standard review process which is the same for documentation and code
(see our [contributing guide](https://www.numpy.org/devdocs/dev/index.html)).
For any new features added to NumPy, comprehensive reference documentation must
be added at the same time as code, including usage examples. We do not have an
overall "documentation work plan" to fix holes in existing documentation and
restructure the documentation for, e.g., easier navigation. The core
development team drives and decides on doc changes as they are proposed; there
is no dedicated "documentation manager" (yet, our project maturity is still
increasing! - see, e.g., our [governance structure](https://www.numpy.org/
devdocs/dev/governance/governance.html)).


**Current documentation**:

- Latest version (tutorial, reference guide, developer docs):
  https://www.numpy.org/devdocs/index.html
- Historical archive of released documentation: https://docs.scipy.org/doc/
- NumPy website (needs work ...): http://www.numpy.org/
- SciPy *ecosystem* website (which NumPy is at the core of): https://scipy.org/
- GitHub repository (all sources for code and docs): https://github.com/numpy/numpy


## Contact

As a community driven project we try to have all conversations about NumPy in
public. The main venue for discussions related to the *development* of NumPy
(which includes GSoD) is the `numpy-discussion` mailing list:
https://scipy.org/scipylib/mailing-lists.html#mailing-lists. Please register
and post to that list for discussing a GSoD proposal or idea. In case you
want to pre-discuss something in private first, please contact the NumPy
GSoD coordinators at numpy-scipy-gsod@googlegroups.com.


## Project idea: High level restructuring and end user focus

NumPy serves many kinds of users: students new to programming or Python,
educators, researchers, domain experts in one of the areas that NumPy covers,
data scientists, library developers, packagers, and more. And NumPy's
documentation is *huge* (the pdf version of the last release is over 1500
pages). **The challenge**: *provide ways to guide those users to the parts of
the documentation most relevant to them.* We would love to work with a
technical writer that is able to help us address this challenge.

**Possible topics** include:
- Improving the structure and content of https://numpy.org/
- Reviewing and improving the structure of the main navigation page of [the
  NumPy documentation](https://www.numpy.org/devdocs/).
- Producing a roadmap or list of work items for engaging the community in
  further documentation work (we have a lot of contributor, channeling their
  energy by setting the right goals and priorities could have a lot of impact).
  This may include making explicit what different kinds of users need to see.
- Rewriting a section of the User Guide (that can then serve as a template for
  other/new sections).
- Adding non-textual images or graphics to enhance the textual explanations
- Updating out-of-date references and refactoring content to latest best
  practices
- Integrating the documentation more cleanly with the growing body of on-line
  literature on scientific computing, data science, resources for learning
  Python, NumPy, and performance considerations when writing code.

We assume that the technical writer who will take on this project is not yet
familiar with NumPy and its community. This means time will need to be built
into the project plan at the start to get familiar with it. Mentors will be
able to provide walkthroughs, set up time for discussing with or interviewing
different kinds of end users and content experts. We are open to listening to
writers' suggestions and contributions. *Some mentors have experience working
with technical writers in a day-job-in-industry setting, but not in an open
source setting - so we'll all learn from each other!*

**Relevant material** that is not yet linked above:

- The [SciPy Lecture Notes](https://scipy-lectures.org/), an external set of
  material specifically aimed at learning/teaching NumPy and the basics of the
  SciPy ecosystem in courses.
- Other NumPy tutorials, from:
  [DataCamp](https://www.datacamp.com/community/tutorials/python-numpy-tutorial),
  [Guru99](https://www.guru99.com/numpy-tutorial.html), [Machine learning
  plus](https://www.machinelearningplus.com/python/numpy-tutorial-part1-array-python-examples/),
  [Stanford CS231](http://cs231n.github.io/python-numpy-tutorial/),
  [Edureka](https://www.edureka.co/blog/python-numpy-tutorial/),
  [Dataquest](https://www.dataquest.io/blog/numpy-tutorial-python/),
  [learnpython.org](https://www.learnpython.org/en/Numpy_Arrays), [Nicolas
  Rougier](https://github.com/rougier/numpy-tutorial), ... (there are many many
  more).
- The [goodreads list](https://www.goodreads.com/shelf/show/python-scipy) of
  books on "python-scipy". Many of those books are about the "SciPy ecosystem",
  which has NumPy at its core.
