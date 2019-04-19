## About Blosc

__Description:__ A very high performance meta-compressor library especially designed for compressing binary data.

__Website:__ http://blosc.org/

__Repositories:__
  * https://github.com/Blosc/c-blosc
  * https://github.com/Blosc/c-blosc2
  * https://github.com/Blosc/Caterva

__Fundamental building blocks for Blosc:__

Blosc is more a denomination for the compression technology used, and it serves as an umbrella for different implementations and applications of the technology.  The libraries that act as the fundamental building blocks of the ecosystem are:

* [C-Blosc](https://github.com/Blosc/c-blosc) is a specialized meta-compressor for binary data (data that usually represents numbers using a fixed amount of bytes).  C-Blosc is designed to bring data to CPU computing units as fast as possible. The Blosc library optimizes compression speed to improve performance for computations on compressed data sets.

* [C-Blosc2](https://github.com/Blosc/c-blosc2) is the next generation of the library. In addition to improved performance, it also offers efficient support for persistency and multiple architectures (Intel and ARM).  The Blosc2 libraries offer major benefits to big data projects interested in leveraging compression in their pipelines.  However, the current documentation, although [pretty formatted](https://blosc-doc.readthedocs.io), is fairly terse and only meant for low-level C developers.

* [Caterva](https://github.com/Blosc/Caterva) is a C library on top of C-Blosc2 that implements a simple multidimensional container for compressed binary data.  It adds the capability to filter, manipulate, and transform data in these containers, either in-memory or on-disk.  This is a young project, so documentation here is still extremely basic.

## The state of Blosc documentation

The traditional documentation for the Blosc library is made via docstrings in the [blosc.h header](https://github.com/Blosc/c-blosc/blob/master/blosc/blosc.h).  The documentation has been refined through the years with the feedback of users, and these were able to contribite directly to its improvement via pull requests. However, while this approach is quite typical for developers using the low level C library, for Blosc2 and Caterva, we would like to improve the not only the quality of the docstrings, but also the accessibility and the visual aspects of it.  In this sense, [C-Blosc2](https://blosc-doc.readthedocs.io/en/latest/) has started this path, but we would like to continue pushing it in this direction further.

## How Blosc documentation is built
 For C-Blosc2, we are using a mix of [Sphinx](http://www.sphinx-doc.org), [doxygen](http://www.doxygen.nl) and [breathe](https://breathe.readthedocs.io).  We then use the [ReadTheDocs](https://readthedocs.org) service so as to render the docs automatically and expose the HTML/PDF output to the public.  For Caterva, we plan to follow a similar approach.

### Current documentation:

* Current version (stable): https://github.com/Blosc/c-blosc/blob/master/blosc/blosc.h
* Latest version for C-Blosc2: https://blosc-doc.readthedocs.io/en/latest/
* Blosc website: http://blosc.org
* GitHub repository (all the projects inside the Blosc umbrella): https://github.com/Blosc

## Contact
The primary communication channels are chat and mailing list, but please feel free to email us ([Francesc Alted](francesc@blosc.org), as GSoD coordinator) if you would like to speak privately.

__Chat:__ https://gitter.im/Blosc/c-blosc

__Mailing List__: blosc@googlegroups.com 

__Email:__ blosc@blosc.org

__Project name:__ Blosc: Handling Compressed Data for Scientists

__Mentors:__ [FrancescAlted](https://github.com/FrancescAlted), [Aleix Alcacer](https://github.com/aleix11alcacer)

## Project idea: Improve the overall quality and make a conceptual overview

We would very much like to improve the quality of the existing documentation for these three projects (C-Blosc, C-Blosc2 and Caterva).  Furthermore, we also want to add a conceptual overview for the projects ansd their underlying commonalities, to give newcomers to the libraries a comprehensive birds-eye view of the Blosc products, and enable them to quickly choose the libraries that suit their use cases and begin developing tools that fit their needs.

In particular, we would like to improve:
* the current API documentation: better structure, new _see also_ sections, and better style and clarity
* conceptual overview and introduction to the libraries
* Blosc/Caterva role in the high-level pipelines.  A tutorial for a high-profile or common use case would be ideal
* assumptions Blosc/Caterva makes about the structure of the data, user, and task
* the relationship between Blosc and libraries built on top, such as PyTables, bcolz or zarr
* How-to guides for compressing, storing and retrieving data in different scenarios

### Similar libraries that we could use as example

* [CURL](https://curl.haxx.se/docs/) is a popular C library that comes with a very complete documentation and it would be a good example to follow.  In particular, the [Using curl to automate HTTP jobs](https://curl.haxx.se/docs/httpscripting.html) chapter is a fine example of how to describe possible applications of a common use case.

* [Zarr](https://zarr.readthedocs.io/en/stable/) is a multidimensional compressed container, but for Python instead of C.  The documentation is very well crafted and it can be a nice source of inspiration too.

### Related material

__Articles__:
* [0] http://blosc.org/pages/blosc-in-depth/
* [1] http://blosc.org/posts/compress-me-stupid/
* [2] http://blosc.org/posts/breaking-memory-walls/
* [3] http://alimanfoo.github.io/2016/09/21/genotype-compression-benchmark.html

__Paper__:
Francesc Alted, ["Why Modern CPUs Are Starving and What Can Be Done about It"](http://www.blosc.org/docs/StarvingCPUs-CISE-2010.pdf) in Computing in Science & Engineering, vol. 12, pp. 68-71, March/April 2010. doi: 10.1109/MCSE.2010.51
