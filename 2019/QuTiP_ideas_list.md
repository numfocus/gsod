# QuTiP project ideas for GSoD'19


**About QuTiP**: QuTiP, the Quantum Toolbox in Python ([qutip.org](http://qutip.org)), has established itself as a major tool in the quantum tech community to study open quantum systems [1,2], which are realistic quantum systems subject to energy loss and decoherence processes, due to their unavoidable interaction with the environment. 


QuTiP allows to efficiently study a broad range of quantum physics processes, such as dissipative dynamics in cavity QED, quantum information processing, quantum optimal control and quantum optics phenomena. The available tools allow the user to describe many-body quantum systems out of equilibrium, superradiance, quantum phase transitions or quantum circuits, among others. 

One of QuTiP's tenets is the Quantum object class (`Qobj`), which wraps data into an object that further describes its properties in a useful way for quantum physicists, for example telling if a matrix is Hermitian or over what tensor-structure the object is defined. QuTiP relies on Numpy, Scipy, Cython and Matplotlib as dependencies.  


Graphical representation is a very important aspect of QuTiP, and the project continuously develops tools that increase the insight into the physical properties of quantum objects. Check out for example this gallery of quantum state representations, including [Schrodinger cat states](https://nbviewer.jupyter.org/github/jrjohansson/qutip-lectures/blob/master/Lecture-16-Gallery-of-Wigner-functions.ipynb). 

**QuTiP and its Community**: QuTiP is maintained by an active community of volunteers. The core team is formed of quantum physics researchers and developers working full-time in academia. A larger community of contributors is represented by students and researchers both in academia, industry and startups in quantum computing, helping each other on GitHub and on the [Google Group](https://groups.google.com/forum/#!forum/qutip). 

There is a growth in open-source software in quantum science and technology research, both in academia and industry. QuTiP is designed to be a general framework for solving quantum mechanics problems such as systems composed of few-level quantum systems and harmonic oscillators. To this end, QuTiP is built from a large (and ever growing) library of functions and classes. 


Firstly released in 2011, QuTiP is a pioneer project in the field of open-source quantum technology and quantum computing [4]. QuTiP has constantly been growing in scope and structure. It includes now many more dynamical solvers and sub-modules. Some of the sub-modules of QuTiP are first released as independent libraries, such as [PIQS](http://piqs.readthedocs.io) [5] while there are also QuTiP plugins, such as [Matsubara](http://matsubara.readthedocs.io) [6]. 


**QuTiP's Impact**: QuTiP is engaging with the other quantum computing and quantum physics libraries, and its impact in the field of quantum technology research is witnessed by the fact that Refs. [1,2] have been cited over 1000 times according to Google Scholar ([1](https://scholar.google.com/scholar?oi=bibs&hl=en&cites=6461191495870975489) and [2](https://scholar.google.com/scholar?cites=12137412545524739721&as_sdt=2005&sciodt=0,5&hl=en)). QuTiP has been downloaded over 100k times on the `conda-forge` channel, via `conda install qutip`, with over 30k downloads via `pip install qutip`. Both citations and downloads have more than doubled in the 2017-2018 span, compared to the whole 2011-2017 period, signalling an accelleration of use and a broadening of the users base.


 QuTiP is engaging the scientific open-source community in Python, and it has been presented at EuroSciPy 2018 in Trento, PyData 2018 in Warsaw, and is currently participating to [GSoC 2019](https://github.com/qutip/qutip/wiki//Google-Summer-of-Code-2019) as an affiliated project of [NumFOCUS](http://qutip.org/news.html). 


**The state of QuTiP's documentation**: 

We have developed a thorough documentation for QuTiP. This entails a User Guide, an API Guide and a unique collection of over 40 tutorials and 20 lectures that are used by students and researchers worlwide to learn and investigate quantum mechanics in real noisy systems, such as current quantum computers, which are inherently noisy quantum systems [3].

Our documentation goes through well-defined standards of review process. In order to facilitate and standardize contribution to QuTiP, we have developed some [development guidelines](https://github.com/qutip/qutip-doc/blob/master/qutip_dev_contrib.md).  We employ best practices in writing PEP8 formatted Python code, as well as sticking to conventions such as PEP 257 for dosctrings. Independent review process is required for the merge. Our tutorials are contained in a [qutip/qutip-notebooks](https://github.com/qutip/qutip-notebooks) folder on Github, and they include technical Development notebooks on benchmarking our functions. Additionally, QuTiP developers have built coherent documentations for other QuTiP-dependent projects: PIQS [5], and Matsubara [6]. 


**How QuTiP's documentation is built**: 

Our documentation is
built with [Sphinx](http://www.sphinx-doc.org) with a theme from [Read the Docs](https://readthedocs.org). We make sure that new .py files have high-quality docstrings written by the contributors, and that these render well in the Sphinx-generated API documentation, generated using readthedocs and hosted on qutip.org. Every time we build a new major release (every few months), we build a new documentation (version currently at 4.3). This is updated with a graph tree of existing code, updated list of contributors, and users guide examples. Alex Pitchford, lead developer, is in charge of the documentation in QuTiP. 

**Current documentation**:

- Latest version of the reference guide:
  http://qutip.org/docs/latest/index.html
- Historical archive of released documentation: http://qutip.org/documentation.html
- QuTiP website: http://www.qutip.org/
- GitHub repository: https://github.com/qutip
- GitHub repository (QuTiP code): https://github.com/qutip/qutip
- GitHub repository (QuTiP documentation): https://github.com/qutip/qutip-doc
- GitHub repository (QuTiP tutorials): https://github.com/qutip/qutip-notebooks


## Contact

QuTiP GSoD coordinator (Alex Pitchford, alex.pitchford@gmail.com). Support will be provided also by other core contributors (Nathan Shammah, nathan.shammah@gmail.com), Shahnawaz Ahmed (shahnawaz.ahmed95@gmail.com) and Eric Giguere (eric.giguere@usherbrooke.ca). 


## Project idea: Upgrade of QuTiP's documentation

The project's documentation needs the following fixes and upgrades:

- The single major task would be fixing current Sphinx incompatibilities, which currently require a tailored setting of dependencies every time the documentation is built. Note that the documentation is built from the `qutip/qutip-doc` and not from the `qutip/qutip` one.

- Enhancement of the graphical presentation of the documentation using Sphinx. 

- Enhancement of the graphical presentation of the documentation on the website, in order to better showcase the many high-level tutorial present in QuTiP, similarly to what is done for scikit-learn (see [https://scikit-learn.org/stable/documentation.html](https://scikit-learn.org/stable/documentation.html) and [https://scikit-learn.org/](https://scikit-learn.org/)).

- Implementation of inter-documentation links using inter-sphinx, in order to activate hyperlinks from QuTiP to its dependencies, e.g., clickable Numpy's function in the User Guide.  

- Tutorials re-organization on the website. We have recently fixed the My Binder settings and would like to emphasize the interactive opportunities even more. 

- A rationalization of the documentation graph would increase the readability. 

All of the previous tasks will not require previous knowledge of QuTiP for their successful completion. We have experience in mentoring students and researchers from the B.Sc. level to the postdoc level and as previous GSoC students and mentors we have well clear the important tasks that maximize a project fruitful progression: communication, guidance, availability, clear deliverables. 


## References
[1] J. R. Johansson, P. D. Nation, and F. Nori: “QuTiP: An open-source Python framework for the dynamics of open quantum systems.”, Comp. Phys. Comm. 183, 1760–1772 (2012)

[2] J. Robert Johansson, Paul D. Nation, and Franco Nori: “QuTiP 2: A Python framework for the dynamics of open quantum systems.”, Comp. Phys. Comm. 184, 1234 (2013)

[3] J. Preskill, "Quantum Computing in the NISQ era and beyond." Quantum **2**, 79 (2018)

[4] Mark Fingerhuth, Tomáš Babej, and Peter Wittek, Open source software in quantum computing, PLoS ONE 13 (12): e0208561 (2018).

[5] N. Shammah, S. Ahmed, N. Lambert, S. De Liberato, and F. Nori, "Open quantum systems with local and collective incoherent processes: Efficient numerical simulation using permutational invariance " Phys. Rev. A 98, 063815 (2018). Code at [http://piqs.readthedocs.io](http://piqs.readthedocs.io)

[6] N. Lambert, S. Ahmed, M. Cirio, and F. Nori, "Virtual excitations in the ultra-strongly-coupled spin-boson model: physical results from unphysical modes", arXiv preprint arXiv:1903.05892. Also [http://matsubara.readthedocs.io](http://matsubara.readthedocs.io)

**Other relevant material**:

- Slides on QuTiP and the quantum-tech open source ecosystem (Nathan Shammah @ Berkeley Lab, 2019). [PDF](https://conferences.lbl.gov/event/195/session/6/contribution/13/material/slides/0.pdf)

- ["The rise of open source in quantum physics research"](http://blogs.nature.com/onyourwavelength/2019/01/09/the-rise-of-open-source-in-quantum-physics-research/), Nathan Shammah and Shahnawaz Ahmed, Nature's physics blog, January 9, 2019. 

- "Bit to QuBit: Data in the age of quantum computers", Shahnawaz Ahmed, PyData 2018, Warsaw, Poland, 2019. [YouTube video](https://www.youtube.com/watch?v=6GAXJhL1mSs).

