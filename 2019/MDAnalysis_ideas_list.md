__Name:__ MDAnalysis

__Description:__ Scientific Python library for the analysis of molecular dynamics simulations in biophysics, chemistry, materials sciences.

__website:__ https://www.mdanalysis.org/

__repository:__ https://github.com/MDAnalysis/mdanalysis

__email:__ <mdnalysis-devel@googlegroups.com> (all developers)

__mentors:__ Oliver Beckstein <orbeckst@gmail.com> (primary contact) and Richard Gowers (<richardjgowers@gmail.com>)

__Project name:__ Make it easy for new users to analyze _their_ data  

__Description:__ MDAnalysis is a Python library that provides an abstract and object-oriented interface to data from particle-based simulations (primarily molecular dynamics simulations), which are widely used for simulating diverse systems such as the interaction of drugs with biomolecules or new materials. MDAnalysis is widely used in the scientific community and is written by scientists for scientists. Feedback from our users indicates that they like using MDAnalysis but wished that the documentation were easier to read and had more examples. The docs for [scikit-learn](https://scikit-learn.org/stable/index.html) and the [PyTorch tutorials](https://pytorch.org/tutorials/index.html) are generally cited as excellent examples of documentation and, taking these as examples, we would like to improve our documentation to make it more accessible and more immediately useful for new users. 

At the moment, the primary sources of information for users are
- the package documentation https://www.mdanalysis.org/docs
- the [basic tutorial](https://www.mdanalysis.org/MDAnalysisTutorial/)
- [example Jupyter notebooks](http://nbviewer.jupyter.org/github/MDAnalysis/binder-notebook/tree/master/notebooks/) (also available as [live binder notebooks](https://mybinder.org/v2/gh/MDAnalysis/binder-notebook/master?filepath=notebooks))
- [Workshop materials](https://www.mdanalysis.org/WorkshopHackathon2018/)
- two [videos](https://www.mdanalysis.org/pages/learning_MDAnalysis/#videos) from conference presentations

We identified two primary areas for improvement (in rank order of priority):

### Restructure docs

We want to **restructure our docs for user-friendliness** [issue #1175](https://github.com/MDAnalysis/mdanalysis/issues/1175) and refactor docs away from how the source code is organized into how the user interacts with the code (started in [PR #1827](https://github.com/MDAnalysis/mdanalysis/pull/1827)). We envision a split into three major blocks:

1. introduction with examples (more like a tutorial) and explanation of the underlying principles and guiding concepts (see the [SciPy 2016 talk](https://www.mdanalysis.org/pages/learning_MDAnalysis/#introductory) and the slides in the presentation [scipy-MDAnalysis-Beckstein.pdf](https://github.com/MDAnalysis/scipy-2016/blob/master/presentation/scipy-MDAnalysis-Beckstein.pdf))
2. API docs (similar to the current docs at https://www.mdanalysis.org/docs/)
3. developer docs (notes for developers, can be technical/arcane)

### Improve and expand tutorials

We have one "official" [introductory tutorial](https://www.mdanalysis.org/MDAnalysisTutorial/) and [various other tutorials](https://www.mdanalysis.org/pages/learning_MDAnalysis/#tutorials) but it is initially confusing to new users what they should look at and it is too long. We need to provide a better "road map" for new users and clearly lay out tutorials for different levels and with clear learning goals. 

We need to split the current [MDAnalysis Tutorial](https://www.mdanalysis.org/MDAnalysisTutorial/) into multiple self-contained tutorials and sort them by level (introductory, intermediate, advanced). The tutorials can and should build on each other. There should be a top level entry point that gives an overview over the tutorials. An initial outline would contain the following (not all content exists yet, especially at intermediate/advanced level):

  1. Introductory level
     1. **Installation**: installing MDAnalysis and testing trajectories (MDAnalysisTests for simple examples, [MDAnalysisData](https://www.mdanalysis.org/MDAnalysisData/) for advanced examples)
     2. **Basic trajectory analysis**: Loading data into a `Universe`, selecting atoms with `Universe.select_atoms()` as an `AtomGroup`, iterating through a trajectory, getting positions from `AtomGroup.positions`, and using numpy operations to calculate observables of interest from the positions.
     3. **Using analysis tools in `MDAnalysis.analysis`**: Performing common analysis tasks such as RMSD calculation and fitting, hydrogen bond analysis, or dihedral analysis using the common analysis classes.
     4. **Working with AtomGroups**: introduction to some often used methods of `AtomGroup` and how to work with multiple AtomGroups; slicing and fancy indexing of `AtomGroup`.
     5. **Writing trajectories**: difference between "trajectories" and "single frame" file formats; standard code pattern for writing trajectories or single frames; writing single frames directly with `AtomGroup.write()`
  2. Intermediate level
     1. **Selections** (requires _Basic trajectory analysis_ and _Working with AtomGroups_): in-depth tutorial on the selection language; dynamically updating selections
     2. **Working with Groups** (requires _Working with AtomGroups_): The "container" hierarchy (`Universe` > `Segment` > `Residue` > `Atom`) and the corresponding groups `SegmentGroup`, `ResidueGroup`, `AtomGroup`: commonalities and differences, aggregating methods. How to work with `fragments` or `molecules`.
     3. **Writing selections**: outputting selections for other codes
     4. **Working with topology information**: introduction to the topology system; how to work with bonds; identify bonded atoms; working with angles and dihedrals; selections by type
     5. **Applying on-the-fly transformations**: A unique capability of MDAnalysis are [trajectory transformations](https://www.mdanalysis.org/docs/documentation_pages/trajectory_transformations.html) that change the trajectory while it is being read and so avoid generating intermediate files that are needed with other analysis packages. This tutorial would be based on the notebook [on-the-fly-transformations.ipynb](https://github.com/MDAnalysis/binder-notebook/blob/master/notebooks/transformations/on-the-fly-transformations.ipynb).
     6. **In-memory trajectories**: how to use the [MemoryReader](https://www.mdanalysis.org/docs/documentation_pages/coordinates/memory.html) to speed up analysis or generate temporary reduced system trajectories for analysis (see, e.g., Workshop notebook [trajectory_magic.ipynb](https://github.com/MDAnalysis/WorkshopHackathon2018/blob/master/01_IntroToMDAnalysis/notebooks/trajectory_magic.ipynb))
     7. **Visualization in notebooks with NGLView**: how to use [nglview](https://github.com/arose/nglview) with MDAnalysis (see Workshop notebook [Visualisation_with_NGLView.ipynb](https://github.com/MDAnalysis/WorkshopHackathon2018/blob/master/06_AdvancedTutorials/Visualisation_with_NGLView.ipynb) and binder notebook [nglview_drawframes.ipynb](https://github.com/MDAnalysis/binder-notebook/blob/master/notebooks/visualization/nglview_drawframes.ipynb))
  3. Advanced level
     1. **System building** (requires _Working with topology information_): how to add atoms or bonds or create simple topologies from scratch; generating initial coordinates
     2. **Extending file reading with own code** (requires _System building_): write a Reader for once own custom file format and dynamically add it to MDAnalysis
     3. **Write your own analysis class**: shows how to leverage the [MDAnalysis.analysis.AnalysisBase](https://www.mdanalysis.org/docs/documentation_pages/analysis/base.html) class to create feature-full custom analysis tools.


For this and other documents we want to start adding example Jupyter notebooks (such as the first few [example notebooks](https://github.com/MDAnalysis/binder-notebook/tree/master/notebooks)) to our sphinx-based restructured text documentation via the [nbsphinx](https://nbsphinx.readthedocs.io/en/0.4.2/) extension.

We also want to **include more diagrams, pictures, and graphs** to make clearer what the relationships between different parts of the code are and what output might look like.
