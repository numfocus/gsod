__Name:__ MDAnalysis

__Description:__ Scientific Python library for the analysis of molecular dynamics simulations in biophysics, chemistry, materials sciences.

__website:__ https://www.mdanalysis.org/

__repository:__ https://github.com/MDAnalysis/mdanalysis

__email:__ mdnalysis-devel@googlegroups.com

__Project name:__ Make it easy for new users to analyze _their_ data  

__Description:__ MDAnalysis is Python library that provides an abstract and object-oriented interface to data from particle-based simulations (primarily molecular dynamics simulations), which are widely used for simulating diverse systems such as the interaction of drugs with biomolecules or new materials. MDAnalysis is widely used in the scientific community and is written by scientists for scientists. Feedback from our users indicates that they like using MDAnalysis but wished that the documentation were easier to read and had more examples. The docs for [scikit-learn](https://scikit-learn.org/stable/index.html) and the [PyTorch tutorials](https://pytorch.org/tutorials/index.html) are generally cited as excellent examples of documentation and, taking these as examples, we would like to improve our documentation to make it more accessible and more immediately useful for new users. 

We identified four areas for improvement (in rank order of priority):

### Restructure docs

We want to **restructure our docs for user-friendliness** [issue #1175](https://github.com/MDAnalysis/mdanalysis/issues/1175) and refactor docs away from how the source code is organized into how the user interacts with the code (started in [PR #1827](https://github.com/MDAnalysis/mdanalysis/pull/1827)). We envisage a split into three major blocks:

1. introduction with examples (more like a tutorial) and explanation of the underlying principles and guiding concepts (see the [SciPy 2016 talk](https://www.mdanalysis.org/pages/learning_MDAnalysis/#introductory) and the slides in the presentation [scipy-MDAnalysis-Beckstein.pdf](https://github.com/MDAnalysis/scipy-2016/blob/master/presentation/scipy-MDAnalysis-Beckstein.pdf))
2. API docs (similar to the current docs at https://www.mdanalysis.org/docs/)
3. developer docs (notes for developers, can be technical/arcane)

### Improve and expand tutorials

We have one "official" [introductory tutorial](https://www.mdanalysis.org/MDAnalysisTutorial/) and [various other tutorials](https://www.mdanalysis.org/pages/learning_MDAnalysis/#tutorials) but it is initially confusing to new users what they should look at and it is too long. We need to provide a better "road map" for new users and clearly lay out tutorials for different levels and with clear learning goals. 

We need to split the current [MDAnalysis Tutorial](https://www.mdanalysis.org/MDAnalysisTutorial/) into multiple self-contained tutorials and sort them by level (introductory, intermediate, advanced). The tutorials can and should build on each other. There should be a top level entry point that gives an overview over the tutorials. An initial outline would contain the following (not all content exists yet, especially at intermediate/advanced):

  1. Introductory level
     1. **Installation**: installing MDAnalysis and testing trajectories (MDAnalysisTests for simple examples, [MDAnalysisData](https://www.mdanalysis.org/MDAnalysisData/) for advanced examples)
     2. **Basic trajectory analysis**: Loading data into a `Universe`, selecting atoms with `Universe.select_atoms()` as an `AtomGroup`, iterating through a trajectory, getting positions from `AtomGroup.positions`, and using numpy operations to calculate observables of interest from the positions.
     3. **Using analysis tools in `MDAnalysis.analysis`**: Performing common analysis tasks such as RMSD calculation and fitting, hydrogen bond analysis, or dihedral analysis using the common analysis classes.
     4. **Working with AtomGroups**: introduction to some often used methods of `AtomGroup` and how to work with multiple AtomGroups; slicing and fancy indexing of `AtomGroup`.
     5. **Writing trajectories**: difference between "trajectories" and "single frame" file formats; standard code pattern for writing trajectories or single frames; writing single frames directly with `AtomGroup.write()`
  2. Intermediate level
     1. **Selections** (requires _Basic trajectory analysis_ and _Working with AtomGroups_): in-depth tutorial on the selection language; dynamically updating selections
     2. **Working with Groups** (requires _Working with AtomGroups_): The "container" hierarchy (`Universe` > `Segment` > `Residue` > `Atom`) and the corresponding groups `SegmentGroup`, `ResidueGroup`, `AtomGroup`: commonalities and differences, aggregating methods. How to work with `fragments`.
     3. **Writing selections**: outputting selections for other codes
     4. **Working with topology information**: introduction to the topology system; how to work with bonds; identify bonded atoms; working with angles and dihedrals; selections by type
  3. Advanced level
     1. **System building** (requires _Working with topology information_): how to add atoms or bonds or create simple topologies from scratch; generating initial coordinates
     2. **Extending file reading with own code** (requires _System building_): write a Reader for once own custom file format and dynamically add it to MDAnalysis
     3. **Write your own analysis class**: shows how to leverage the [MDAnalysis.analysis.AnalysisBase](https://www.mdanalysis.org/docs/documentation_pages/analysis/base.html) class to create feature-full custom analysis tools.

For this and other documents we want to start adding example Jupyter notebooks (such as the first few [example notebooks](https://github.com/MDAnalysis/binder-notebook/tree/master/notebooks)) to our sphinx-based restructured text documentation via the [nbsphinx](https://nbsphinx.readthedocs.io/en/0.4.2/) extension.

We also want to **include more diagrams, pictures, and graphs** to make clearer what the relationships between different parts of the code are and what output might look like.

### Howto Library

We wand to create a library of short *Howtos* (mini-tutorials) that quickly show to obtain a specific result. The ideal format are Jupyter Notebooks with runable code. We already have a few [example notebooks](https://github.com/MDAnalysis/binder-notebook/tree/master/notebooks) that can [run on Binder](https://mybinder.org/v2/gh/MDAnalysis/binder-notebook/master?filepath=notebooks) but we are not covering a sufficient range of examples and examples might be outdated. Ideally we would regularly test if the notebooks still work.

1. Developers need to identify a small number of "FAQ" cases that would make for good small self-contained Howtos
2. Initial selection of examples
     - B-factor coloring
     - PDB file manipulation (e.g. adding ChainIDs)
     - selections with updating AtomGroups
     - trajectory conversion
     - RMSD analysis
     - RMSF analysis
     - dihedral analysis
3. Jupyter notebooks need to be written that solve the problem. These notebooks should use example data and should be executable on binder. They can use either data files from MDAnalysisTests or MDAnalysisData.
4. For each case, a short HowTo document (in restructured text and processed with sphinx) needs to be written that 
   - links to installation instruction and introductory tutorials (basically: all the things one needs to know)
   - integrates the notebook in the documentation via the [nbsphinx](https://nbsphinx.readthedocs.io/en/0.4.2/) extension (which is important because nothing is more annoying than having to leave the docs to switch to a notebook viewer)

### Background and Algorithms

Loosely connected to the introductory section of the tutorial, we would like to build up a more extensive and in-depth document on the algorithms and data structures. This would be more scholarly and could conceivably expanded into a paper on fundamentals of analysing MD simulations. It would required more diagrams and graphs and more emphasis on citations. Topics to be included:

1. algorithms for distance calculations, including treatment of periodic boundaries: difference between `distance_array` and `self_distance_array` as well as `capped_distance_array`; how `calc_bonds` works.
2. Treatment of periodic boundaries in different contexts; wrapping/unwrapping of molecules
3. algorithms for commonly performed analyses
   - hydrogen bonds and hydrogen bond correlations
   - RMSD
   - RMSF
   - contacts
   - dihedrals and Ramachandran plots
   - PCA
   - radial distribution functions and volumetric densities


