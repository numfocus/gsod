## About
__Name:__ matplotlib.org

__Description:__ Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms.

__Website:__ https://matplotlib.org/

__Repository:__ https://github.com/matplotlib/matplotlib

__How to Document__: https://matplotlib.org/devel/documenting_mpl.html

## Contact
The primary contact with the group is via chat and mailing list, but please feel free to email us if you would like to speak privately. 

__Chat:__ https://gitter.im/matplotlib/matplotlib

__Mailing List__:	matplotlib-devel@python.org

__Email:__ matplotlib@numfocus.org

## Project
We welcome proposals for all things documentation, including but not at all limited to the project listed here. We strongly believe you've probably got a better [handle on how to fix our docs](https://numfocus.org/blog/matplotlib-lead-developer-explains-why-he-cant-fix-the-docs-but-you-can) than we do.

__Project name:__ Matplotlib for Data Scientists

__Mentors:__ [story645](https://github.com/story645/), [@tacaswell](https://github.com/tacaswell)

__Description:__ Matplotlib was primarily develped by scientists for scientific visualization, and modeled on scientific computation langauges such as Matlab, but one of the fastest growing audiences for Matplotlib is data science practitioners. To address the needs of this audience, we propose developing a conceptual overview (such as [2-4] listed below) oriented at newcomers to scientific visualization. 

The overview would possibly cover topics such as:
* the visualization pipeline: data->transformation->chart [1]
* matplotlib's role in the pipeline , i.e. that it's a low level library [7,2,3]
* assumptions matplotlib makes about the structure of the data, user, and task
* matplotlib's imperative architecture and how that differs from declarative libraries like ggplot [5]
* the relationship between matplotlib and libaries built on top, such as Pandas and Seaborn [5, 8, 9] 
* terminology that can be confusing or is used inconsistently (ex norm and colormap on images, tickers/locators) [5]
* how to customize the plots created by libraries like Pandas and Seaborn

These topics, and the scope, are expected to change as the overview develops and we welcome suggestions by the technical writer on approaches for addressing this audience. 

__Paper__: (email for copy)
J. D. Hunter, "Matplotlib: A 2D Graphics Environment," in Computing in Science & Engineering, vol. 9, no. 3, pp. 90-95, May-June 2007.
doi: 10.1109/MCSE.2007.55
URL: http://ieeexplore.ieee.org.ccny-proxy1.libr.ccny.cuny.edu/stamp/stamp.jsp?tp=&arnumber=4160265&isnumber=4160244

__Related material__:
* [1] https://infovis-wiki.net/wiki/Visualization_Pipeline
* [2] https://medium.com/@Elijah_Meeks/d3-is-not-a-data-visualization-library-67ba549e8520
* [3] https://towardsdatascience.com/a-comprehensive-guide-to-the-grammar-of-graphics-for-effective-visualization-of-multi-dimensional-1f92b4ed4149
* [4] https://scikit-learn.org/stable/tutorial/basic/tutorial.html
* [5] https://github.com/matplotlib/AnatomyOfMatplotlib
* [6] https://matplotlib.org/tutorials/introductory/lifecycle.html
* [7] https://matplotlib.org/tutorials/introductory/usage.html#sphx-glr-tutorials-introductory-usage-py
* [8] https://towardsdatascience.com/customizing-plots-with-python-matplotlib-bcf02691931f
* [9] https://towardsdatascience.com/a-step-by-step-guide-for-creating-advanced-python-data-visualizations-with-seaborn-matplotlib-1579d6a1a7d0

__Project name:__ Matplotlib Cheetsheets

__Mentors:__ [story645](https://github.com/story645/), [@tacaswell](https://github.com/tacaswell)

__Description:__ Matplotlib provides a comprehensive gallery of examples [1], but the sheer number of examples can be overwhelmng and the coding heavy orientation can leave users really wanting a little bit of context. We propose a series of cheatsheets that provide some contextual knowledge, modeled on the Pandas and GGplot sheets [2,3], that users can use as references for common tasks in Matplotlib. 

The cheetsheets would be on topics such as:
* terminology that can be confusing or is used inconsistently (ex norm and colormap on images, tickers/locators) 
* elements of a matplotlib figure [4]
* making the basic chart types - pie, bar, line, scatter, heatmap [10]
* marker and line customization [5-8]
* color - what is a norm, a colormap [9]
* text labels and annotations [11, 12]
* subplots and layouts [13] 
* animation [14]
* how to customize the plots created by libraries like Pandas and Seaborn [15]

The expectation is some of these topics could possibly be combined into one cheatsheet and some sheets may overlap - deep dive versus surface - and we hope the technical writer will help prevent us from making overwhelming reference sheets. We also hope the technical writer will help identify other topics that may make for good cheetsheets. 

__Related material__:
* [1] https://matplotlib.org/gallery/index.html
* [2] https://github.com/rstudio/cheatsheets/blob/master/data-visualization-2.1.pdf
* [3] https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf
* [4] https://matplotlib.org/gallery/showcase/anatomy.html#sphx-glr-gallery-showcase-anatomy-py
* [5] https://matplotlib.org/gallery/lines_bars_and_markers/linestyles.html#sphx-glr-gallery-lines-bars-and-markers-linestyles-py
* [6] https://matplotlib.org/gallery/lines_bars_and_markers/line_styles_reference.html#sphx-glr-gallery-lines-bars-and-markers-line-styles-reference-py
* [7] https://matplotlib.org/gallery/lines_bars_and_markers/marker_reference.html#sphx-glr-gallery-lines-bars-and-markers-marker-reference-py
* [8] https://matplotlib.org/gallery/lines_bars_and_markers/marker_fillstyle_reference.html#sphx-glr-gallery-lines-bars-and-markers-marker-fillstyle-reference-py
* [9] [https://matplotlib.org/gallery/index.html#color
* [10] https://github.com/matplotlib/matplotlib/issues/7956#issuecomment-275518231
* [11] https://matplotlib.org/gallery/index.html#text-labels-and-annotations
* [12] https://matplotlib.org/gallery/index.html#ticks-and-spines
* [13] https://matplotlib.org/tutorials/intermediate/gridspec.html#sphx-glr-tutorials-intermediate-gridspec-py
* [14] https://matplotlib.org/gallery/index.html#animation
* [15] https://towardsdatascience.com/a-step-by-step-guide-for-creating-advanced-python-data-visualizations-with-seaborn-matplotlib-1579d6a1a7d0
