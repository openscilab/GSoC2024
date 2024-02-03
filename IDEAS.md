# OpenSciLab Project Ideas for Google Summer of Code
Here are ideas for improving OpenSciLab projects.
For each project, there are multiple ideas with a title and a short description fetched from our backlog. Each of these ideas could have some tasks. Based on our evaluation, for each contributor it will take 3.5 month (nearly what GSoC is also planned to) to fulfill an idea's objectives. 

## [PyCM: Multi-class confusion matrix library in Python](https://github.com/sepandhaghighi/pycm)
<div align="center">
    <img src="https://github.com/sepandhaghighi/pycm/raw/master/Otherfiles/logo.png" width="400">
</div>

#### Mentor(s)
* [Sadra Sabouri](https://sadrasabouri.github.io/)
* [Arash Zolanvari](https://alirezazolanvari.github.io/)

PyCM is a multi-class confusion matrix library written in Python that supports both input data vectors and direct matrix, and a proper tool for post-classification model evaluation that supports most classes and overall statistics parameters. The project has been developed for six years and matured enough. Now there is time to add new features enlarging the library scope.

### Dissimilarity/Distance Matrix and Incidence Matrix
In classification setting, a dissimilarity matrix quantifies the dissimilarity between pairs of classes. The idea is to add support for dissimilarity matrix and provide a pipeline, such as what we have now for `ConfusionMatrix`, extracting various related metrics.

Incidence matrix is a logical matrix showing relationship between classes of objects. In classification setting, it can be useful in cases which two classes are too similar so that makes it hard for classifier to classify it. Adding support for this matrix and its metrics could ease the path for researchers to continue their studies on it.

* If you are interested into software development scaling challenges and also like research metrics in machine learning, this idea could be your best shot.

### I/O Enhancement
As time goes on, there where situation in which users wanted to import their data or get their output from a format which we didn't have plan for supporting it. This idea will target aggregation of challenging input/output formats which was desired to be supported by PyCM. Following we have our objectives for this idea.

1. Support `csv` files as input
2. Support `.md` format as output
3. Support `LateX` format as output
4. HTM format output enhancement

* If you are interested in system/pipeline design and ready to dig into parsing these formatted structure, let's pick p this idea.

### Curve Generalization and Threshold Selection

### Data Distribution Analysis

### PyCM Optimization: Boosting Performance & Speed and Software Structure Enhancement

### Make PyCM More Accessible to Data Scientists (Documentation)

### Incorporate Time Series Analysis in PyCM for Dynamic Model Assessment

### Real-time Model Monitoring with PyCM

## [PyRGG: 🔧 Python Random Graph Generator](https://github.com/sepandhaghighi/pyrgg)
<div align="center">
    <img src="https://github.com/sepandhaghighi/pyrgg/raw/master/otherfile/logo.png" width="400">
</div>

#### Mentor(s)
* [Sadra Sabouri](https://sadrasabouri.github.io/)
* [Arash Zolanvari](https://alirezazolanvari.github.io/)

PyRGG is a command-line-interface (CLI) tool for generating random graphs. This tool supports various graph format including `DIMACS(.gr)` files. PyRGG is being used in broad range of graph-based research applications.

### Add New Graph Generation Model
In computer science and network analysis, random graphs are frequently employed to simulate and study the structure of networks, such as social networks, communication networks, and the internet. These generated graphs serve as benchmarks for evaluating algorithms, assessing network resilience, and studying the properties of large-scale networks. Additionally, in bio-informatics, random graphs are utilized to model biological interactions, enabling the analysis of complex biological networks. PyRGG is a tool for generating random graph via Python. There are several random graph generation models. Currently PyRGG supports two models (which are `pyrgg` and `Erdős–Rényi-Gilbert model - G(n,p)` method). The idea is to implement all existing methods for random graph generation, a non exhaustive list of those methods are in below:

1. Erdős–Rényi model - G(n,M)
2. Barabási–Albert model
3. Watts–Strogatz model
4. Exponential family random graph models
5. Stochastic block model

* If you are looking for a hands-on research experience on random graph generation, this idea is yours.

### Make PyRGG More Accessible for Researchers
PyRGG is a command-line-interface (CLI) application. Although we tried to make user interface as simple as possible, there is a long way to go. Use-cases could range from Python package APIs to graphical interfaces, that means we should have both form out python package level abstraction and button-textbox view for random graph generation. Plus that, integration to existing graph analysis Python libraries needed to be show-cased as a blog-post or in documentation. These examples usually works as boilerplate for researchers when using Python libraries.

1. Showcase integration with existing graph libraries (such as `networkx`)
2. Generalize package's functions making them able to serve as a Python library API
3. Development of a simple graphical user interface

* If you are looking for documenting, blogging and user experience design, you should write a proposal on this idea.
