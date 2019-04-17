## About
__Name:__ blosc.org

__Description:__ A very high performance meta-compressor library especially designed for compressing binary data.

__Website:__ http://blosc.org/

__Repositories:__
  * https://github.com/Blosc/c-blosc
  * https://github.com/Blosc/c-blosc2
  * https://github.com/Blosc/Caterva

__Current docs:__ https://blosc-doc.readthedocs.io

## Contact
The primary communication channels are chat and mailing list, but please feel free to email us if you would like to speak privately. 

__Chat:__ https://gitter.im/Blosc/c-blosc

__Mailing List__: blosc@googlegroups.com 

__Email:__ blosc@blosc.org

__Project name:__ Blosc: Handling Compressed Data for Scientists

__Mentor:__ [FrancescAlted](https://github.com/FrancescAlted)

__Description:__ C-Blosc is a specialized meta-compressor for binary data (data that usually represents numbers using a fixed amount of bytes).  C-Blosc is designed to bring data to CPU computing units as fast as possible. The Blosc library optimizes compression speed to improve performance for computations on compressed data sets.

[C-Blosc2](https://github.com/Blosc/c-blosc2) is the next generation of the library. In addition to improved performance, it also offers efficient support for persistency and multiple architectures (Intel and ARM).  The Blosc2 libraries offer major benefits to big data projects interested in leveraging compression in their pipelines.  However, the current documentation, although [pretty formatted](https://blosc-doc.readthedocs.io), is fairly terse and only meant for low-level C developers.

[Caterva](https://github.com/Blosc/Caterva) is a C library on top of C-Blosc2 that implements a simple multidimensional container for compressed binary data.  It adds the capability to filter, manipulate, and transform data in these containers, either in-memory or on-disk.  This is a young project, so documentation here is still extremely basic.

We would very much like to improve the quality of the existing documentation for these three projects (C-Blosc, C-Blosc2 and Caterva).  Furthermore, we also want to add a conceptual overview for the projects ansd their underlying commonalities, to give newcomers to the libraries a comprehensive birds-eye view of the Blosc products, and enable them to quickly choose the libraries that suit their use cases and begin developing tools that fit their needs.

In particular, we would like to improve:
* the current API documentation: better structure, new _see also_ sections, and better style and clarity
* conceptual overview and introduction to the libraries
* Blosc/Caterva role in the high-level pipelines.  A tutorial for a high-profile or common use case would be ideal
* assumptions Blosc/Caterva makes about the structure of the data, user, and task
* the relationship between Blosc and libraries built on top, such as PyTables, bcolz or zarr
* How-to guides for compressing, storing and retrieving data in different scenarios

__Paper__:
Francesc Alted, "Why Modern CPUs Are Starving and What Can Be Done about It" in Computing in Science & Engineering, vol. 12, pp. 68-71, March/April 2010. doi: 10.1109/MCSE.2010.51
* URL1: https://www.computer.org/csdl/magazine/cs/2010/02/mcs2010020068/13rRUxBa5fz
* URL2: http://www.blosc.org/docs/StarvingCPUs-CISE-2010.pdf


__Related material__:
* [0] http://blosc.org/pages/blosc-in-depth/
* [1] http://blosc.org/posts/compress-me-stupid/
* [2] http://blosc.org/posts/breaking-memory-walls/
* [3] http://alimanfoo.github.io/2016/09/21/genotype-compression-benchmark.html
