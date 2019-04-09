**TODO** – flesh out, this is an initial draft based on [MDAnalysis Wiki: Google Season of Docs](https://github.com/MDAnalysis/mdanalysis/wiki/Google-Season-of-Docs) (@orbeckst)

Feedback from our users indicates that they like to use MDAnalysis but wished that the documentation were easier to read and had more examples. The docs for [scikit-learn](https://scikit-learn.org/stable/index.html) and the [PyTorch tutorials](https://pytorch.org/tutorials/index.html)  are generally cited as excellent examples of documentation. 

1. [restructure docs for user-friendliness](https://github.com/MDAnalysis/mdanalysis/issues/1175): 
   1. introduction with examples (more like a tutorial)
   2. API docs (similar to the current docs at https://www.mdanalysis.org/docs/)
   3. developer docs (notes for developers, can be technical/arcane)
2. improve tutorials
   - split https://www.mdanalysis.org/MDAnalysisTutorial/ into introductory and intermediate level and extend as necessary
   - add tutorials that include the notebooks from https://github.com/MDAnalysis/binder-notebook/tree/master/notebooks via the [nbsphinx](https://nbsphinx.readthedocs.io/en/0.4.2/) extension
3. short *Howto* mini-tutorials
   - developers need to identify a small number of "FAQ" cases that would make for good small self-contained Howto
   - examples
     - B-factor coloring
     - PDB file manipulation (e.g. adding ChainIDs)
     - selections with updating AtomGroups
     - trajectory conversion
     - RMSD analysis
     - RMSF analysis
     - dihedral analysis

