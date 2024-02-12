# OpenSciLab Project Ideas for Google Summer of Code
Here are ideas for improving OpenSciLab projects.
Each project has multiple ideas with a title and a short description fetched from our backlog. Each of these ideas could have some tasks. We provided an expected time for each of these ideas.

## [PyCM: Multi-class confusion matrix library in Python](https://github.com/sepandhaghighi/pycm)
<div align="center">
    <img src="https://github.com/sepandhaghighi/pycm/raw/master/Otherfiles/logo.png" width="400">
</div>

#### Mentor(s)
* [Sadra Sabouri](https://sadrasabouri.github.io/)
* [Arash Zolanvari](https://alirezazolanvari.github.io/)

PyCM is a multi-class confusion matrix library written in Python that supports input data vectors and direct matrix and a proper tool for post-classification model evaluation that supports most classes and overall statistics parameters. The project has been developed for six years and has matured enough. Now there is time to add new features enlarging the library scope.

### Dissimilarity/Distance Matrix and Incidence Matrix
In classification setting, a dissimilarity matrix quantifies the dissimilarity between pairs of classes. The idea is to add support for dissimilarity matrix and provide a pipeline, such as what we have now for `ConfusionMatrix`, extracting various related metrics.

The incidence matrix is a logical matrix showing the relationship between classes of objects. In the classification setting, it can be helpful in cases where two classes are too similar, making it hard for a classifier to classify them. Adding support for this matrix and its metrics could ease the path for researchers to continue their studies.

* If you are interested in software development scaling challenges and also like research metrics in machine learning, this idea could be your best shot.

### I/O Enhancement
As time went on, there were situations in which users wanted to import their data or get their output from a format that we didn't have a plan for supporting it. This idea will target the aggregation of challenging input/output formats, which was desired to be supported by PyCM. We have our objectives for this idea as follows.

1. Support `csv` files as input
2. Support `.md` format as output
3. Support `LateX` format as output
4. HTM format output enhancement

* If you are interested in system/pipeline design and ready to dig into parsing these formatted structures, let's pick up this idea.

### Curve Generalization
A class of classification problems outputs a probability distribution over all classes for each sample. In those cases, you can define a threshold for your classification, i.e., given a sample, if the probability associated with a class was higher than that threshold, classify it as that class. Curves are pointing out trade-offs between different metrics when changing that threshold. One of the most famous curves is the ROC curve, supported by PyCM from version `3.7`. Here we wanted to change the PyCM's `Curve` class into something more general, where you can easily plot each of the two metrics based on each other.

1. Generalize `Curve` class
2. Add `P-Curve`
3. Add `R-Curve`
4. Add `F1-Curve`

* Let's propose this idea if you want hands-on research experience on machine learning evaluation metrics. We would love to hear more about your ideas.

### Threshold Selection
When your classification model outputs probability distribution over all possible classes instead of labels, you can classify by defining a threshold for your classification, i.e., given a sample, if the probability associated with a class was higher than that threshold, classify it as that class.
Finding the best threshold for a classification problem usually involves a trade-off between metrics. Let's think of a probabilistic model that tells you if you have COVID-19. If you strictly set the threshold high, while you can be more sure about cases classified as infected, you probably miss some truly infected cases. This trade-off makes it uneasy to find the best threshold for a problem. Here we propose a best-effort solution for finding the best threshold in PyCM.

* If you want to have a hands-on research experience on machine learning and learn more about different threshold suggestion methods, let's try this idea.

### Comparing Classification Models
PyCM introduced a method to compare several confusion matrices. You can compare the results of two classification methods by comparing their confusion matrices sharing a ground truth vector. Earlier implementation of the `Compare` object in Version `2.0` hasn't been updated since then. Here we wanted to enhance the implementation of that object and add new methods for comparing confusion matrices.

* If you are interested in pure confusion matrix research and software architecture enhancement, start here.

### Benchmark Tests
Benchmarking PyCM performance over different hardware and inputs would benefit our analysis. It would help us discover bottlenecks and make it easier for us to scale the framework. A non-exhaustive list of analyses we want is listed here. You can think beyond this list and design a complete benchmark testing for PyCM.

1. Testing PyCM performance on different hardware settings
2. Testing PyCM performance on different input sizes
3. Testing PyCM different API calls
4. Security tests

* If you are looking for a set of software testing tasks and QA tasks, let's try this idea.

### Data Distribution Analysis
When evaluating a classifier, you can infer information about the data distribution. Until now, we have been agnostic toward sample distribution for our metric extraction. Here, we want first to identify ways to understand sample data distribution. Then, we add information regarding sample distribution to PyCM output and explore for more metrics that utilize the given data distribution.

* This one suits you if you are interested in probability theories and hands-on experiences.

### PyCM Optimization: Boosting Performance & Speed and Software Structure Enhancement
Every open-source software project that has evolved through time eventually finds some sub-optimality in its implementation. Technical debts and poor implementation could open opportunities for software engineers to enhance the project's performance and software architecture. The idea here is to start by identifying potential bottlenecks in the codebase and write down your proposal on your solution for them.

* If you are a software developer who wants to challenge yourself by diving into source code and looking for flaws, let's do this.

### Make PyCM More Accessible to Data Scientists
PyCM has been used vastly by researchers since the start of the project, but it has yet to be used by data scientists. Although the `scikit-learn` library has a naive implementation for confusion matrices with a minimum number of metrics. Data scientists just rely on that and don't go further to use more advanced tools like PyCM. In this idea, we first wanted to identify why that is happening. Then we wanted to remove barriers so data scientists could use PyCM easily in their projects. The following tasks may be needed to fulfill this idea.

1. Conduct a survey/interview among data scientists to find out about barriers
2. Coming up with solutions
3. Blogging show-cases in which using PyCM is helping with a better understanding of a classification problem
4. Design a website for online PyCM use-cases

* This is for you if you are interested in human-subject research and user experience design.


## [PyRGG: 🔧 Python Random Graph Generator](https://github.com/sepandhaghighi/pyrgg)
<div align="center">
    <img src="https://github.com/sepandhaghighi/pyrgg/raw/master/otherfile/logo.png" width="400">
</div>

#### Mentor(s)
* [Sadra Sabouri](https://sadrasabouri.github.io/)
* [Arash Zolanvari](https://alirezazolanvari.github.io/)

In computer science and network analysis, random graphs are frequently employed to simulate and study the structure of networks, such as social networks, communication networks, and the Internet. These generated graphs serve as benchmarks for evaluating algorithms, assessing network resilience, and studying the properties of large-scale networks. In bio-informatics, random graphs are utilized to model biological interactions, enabling the analysis of complex biological networks. PyRGG is a command line interface (CLI) tool for generating random graphs. This tool supports various graph formats, including `DIMACS(.gr)` files. PyRGG is being used in a broad range of graph-based research applications.

### Add New Graph Generation Model
There are several random graph generation models. Currently, PyRGG supports two models (which are `pyrgg` and `Erdős–Rényi-Gilbert model - G(n,p)` method). The idea is to implement all existing methods for random graph generation; a non-exhaustive list of those methods is in below:

1. Erdős–Rényi model - G(n,M)
2. Barabási–Albert model
3. Watts–Strogatz model
4. Exponential family random graph models
5. Stochastic block model

* If you want hands-on research experience on random graph generation, this idea is yours.

### Make PyRGG More Accessible for Researchers
PyRGG is a command-line interface (CLI) application. Although we tried to make the user interface as simple as possible, there is a long way to go. Use cases could range from Python package APIs to graphical interfaces, which means we should have both form out Python package level abstraction and button-textbox view for random graph generation. Plus, integration to existing graph analysis Python libraries must be showcased as a blog post or in documentation. These examples usually work as a boilerplate for researchers when using Python libraries.

1. Showcase integration with existing graph libraries (such as `networkx`)
2. Generalize the package's functions, making them able to serve as a Python library API
3. Development of a simple graphical user interface

* If you are looking for documenting, blogging, and user experience design, you should write a proposal regarding this idea.
