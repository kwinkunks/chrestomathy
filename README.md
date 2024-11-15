# chrestomathy

A collection of notebooks exploring various ways to do some scientific and statistical calculations, with a bit of a geoscience flavour to some of them.


## Same nail, different hammers

A **crestomathy** is, according to [Wikipedia](https://en.wikipedia.org/wiki/Chrestomathy):

> A chrestomathy (from the Ancient Greek χρηστός, khrēstós, meaning "useful", and μανθάνω, manthánō, meaning "learn") is a collection of selected literary passages [...]; a selection of literary passages from a foreign language assembled for studying the language; or a text in various languages, used especially as an aid in learning a subject. [...] It is different from an anthology because of its didactic purpose.

Each notebook in this unstructured collection explores a different goal, such as performing linear regression on some data, gridding irregular data to make a map (also a regression), or solving a linear algebraic equation. Each exploration involves stating the problem, then looking at different ways to do it, usually in increasingly sophisticated ways.


## Notebooks

### 🥨 Maths and stats flavour

- [Averages](notebooks/Averages.ipynb) ✨ **New**
- [Activation functions](notebooks/Activation_functions.ipynb) ✨ **New**
- [Function differentiation](notebooks/Function_differentiation.ipynb) ✨ **New**
- [Timeseries extrapolation](notebooks/Timeseries_extrapolation.ipynb) ✨ **New**
- [Linear regression](notebooks/Linear_regression.ipynb)
- [Regression algorithms](notebooks/Regression_algorithms.ipynb)
- [Curse of dimensionality](notebooks/Curse_of_dimensionality.ipynb) ✨ **Updated**

### ⚒️  Geoscience flavour

- [Map interpolation](notebooks/Map_interpolation.ipynb)
- [Unsupervised clustering](notebooks/Unsupervised_clustering.ipynb) (of rock properties)
- [Phase determination](notebooks/Phase_determination.ipynb) (of seismic data)
- [Wavelet estimation](notebooks/Wavelet_estimation.ipynb) (from wells and seismic)


## Suggested additions

Topics for the future:

- Ways to represent points in 2-space, very useful for Advent of Code (eg [2018 Day 10 one](https://github.com/kwinkunks/aoc18/blob/master/day10.py)):
  - Implicit position using counters or enumeration in loops
  - `tuple(x, y)` or `tuple(col, row)`
  - `complex(x, y)`
  - `Point` class...
  - ...with `functools.total_ordering`, operator overloading, etc
  - `shapely.Point` class
- Different ways to make a normal distribution (and/or other distributions as well perhaps).
- Sorting algorithms, but this has been done many times before.
- Pathfinding algorithms, but this is probably beyond me since I've never managed those problems in Advent of Code :D
- Binary classification algorithms: probably can't beat [scikit-learn's comparison](https://scikit-learn.org/1.5/auto_examples/classification/plot_classifier_comparison.html) though.
- Multiclass classification algorithms, using rock property catalog data, and with the multi-class decision surface visualization [from Agile](https://github.com/agilescientific/geocomputing/blob/develop/prod/Classification_algorithms.ipynb).
- Clustering algorithms (or maybe just add to or generalize the existing notebook), but again [sklearn's comparison](https://scikit-learn.org/1.5/auto_examples/cluster/plot_cluster_comparison.html) is totally awesome.
- Data assimilation methods, although quite technical, and probably already perfectly well done by, eg, [`dapper`](https://github.com/nansencenter/DAPPER)
- Bayesian parameter estimation is perhaps more approachable than data assimilation.
- Distance algorithms are a huge subject &mdash; some of these topics deserve whole notebooks to themselves. There are plenty to choose from.
  - All the Minkowski distances (L0, L1 L2, etc) and maybe octile distance
  - Coherence etc for seismic
  - Levenshtein edit distance for words
  - Canberra distance for ranked lists and other things https://en.wikipedia.org/wiki/Canberra_distance
  - Word/doc embedding distance (embeddings and latent spaces in general), eg https://www.andrew.cmu.edu/course/15-121/labs/HW-4%20Document%20Distance/lab.html
  - Pixel and Image distance, eg see below
  - Clock distance (23:55 and 00:05 are very close, use circular distance eg https://gist.github.com/anonymous/7ce6274c630dabd70960c6d7fdd6c580
  - Wasserstein aka Earth mover’s distance for distributions https://en.wikipedia.org/wiki/Earth_mover%27s_distance
  - Probably some others: https://en.wikipedia.org/wiki/Metric_(mathematics)
  - 3D shapes, eg https://arxiv.org/pdf/1911.09204.pdf
  - See table here > https://stats.stackexchange.com/questions/58706/distance-metrics-for-binary-vectors/386952
  - Well logs could use cross-correlation, say. Also see https://quant.stackexchange.com/questions/848/time-series-similarity-measures
  - Curves: Hausdorff distance (no order info), Frechet distance (dog leash distance), dynamic time-warp distance (not a metric as doesn’t meet triangle inequality condition), eg see https://www.youtube.com/watch?v=mxat0UbmDo0
  - Dynamic time warping would be fun to explore; most of the algorithms are closely related.
