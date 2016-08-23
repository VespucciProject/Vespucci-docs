---
layout: page
title: "Vespucci User Interface"
category: gs
date: 2016-07-05 16:21:24
---


The vespucci user interfact consists of 6 sections, shown below.

![Vespucci-UI](http://vespucciproject.org/Vespucci-docs/img/Vespucci_UI1.png)

Each section will be described briefly, then in more detail.

**A. Menu Bar**

The menu bar contains all of the general commands for controlling Vespucci: dataset import/export, manipulation, etc. On a Mac OS, this is at the top of the screen.

**B. Toolbar**

The toolbar contains a group of shortcuts for frequent actions in Vespucci.

**C. Dataset Navigator**

The dataset navigator is used to move through the dataset and any added elements, such as a multivariate analysis.

**D. Spectrum Viewer**

The spectrum viewer allows one to view the individual indices of a map (a map is a 2-dimensional grid, with point spectra at each point on the grid).

**E. Data Viewer**

The data viewer allows one to view the actual values for a matrix one selects in the dataset navigator.

**F. Plot Viewer**

The plot viewer is used to view any two elements, most frequently spectra, but occasionally other elements such as PCA (Principle Components Analysis) loadings.


### Menu Bar

The menu bar contains 8 elements.

**File** - this contains straightforward commands regarding importing/exporting datasets, as well as saving/opening files in Vespucci's filetype.


**Dataset** - this contains straightforward commands regarding a single dataset. 

"New Composite Dataset" allows one to combine datasets into a new dataset (spectra can be concatenated, or averaged together).

"New Dataset From Matrix" allows one to select individual elements of an analysis, and then form a new dataset from that (as an example, selecting a single cluster assignment from a k-means analysis to form a dataset).


**Matrix** - this contains options for manipulating specific matrices within the dataset.

"Analyze" allows one to perform several multivariate analyses on a single matrix, rather than an entire dataset.

"Transform" allows one to perform a simple transform operation on a single matrix.


**Processing** - this contains commands for dataset manipulation such as baseline correction or normalization. Refer to the Processing page for more information.

**Analysis** - this contains commands for extrapolating information from the dataset, such as k-means cluster analysis or a univariate analysis.

"Calculate Representative Spectrum" creates a single spectrum based off of all others in the dataset. Each wavenumber value can be determined in two different ways: by taking the average of each spectrum's wavenumber value, and by taking the median of of each spectrum's wavenumber value. Additionally, each spectrum will be compared to the representative spectrum (based on a selected distance metric) to find the one most similar to the representative spectrum.

"On Multiple Datasets" performs an analysis on multiple datasets. This temporarily concatenates the datasets to perform an analysis, giving combined results. The results are then separated out for each dataset, giving results specific to an individual dataset which incorporated the entire group of datasets in the analysis.


**Tools** - this contains simple settings for Vespucci.

**Window** - this shows various dialogs of Vespucci which can be enabled as needed. The most commonly used dialogs are enabled automatically. New dialogs are opened in a new window, rather than as a part of the standard Vespucci window.

** 

**Help** - This contains information about using Vespucci.


### Toolbar

The toolbar contains 8 elements, described below.

**Open Dataset** - opens a file saved in the Vespucci format (.h5).

**Save Dataset** - saves the dataset in the Vespucci format.

**Import Dataset** - imports a single dataset. This is described in more detail on the "Importing Data" page.

**Import Datasets** - imports multiple "point spectra" datasets. This is described in more detail on the "Importing Data" page.

**Close Dataset** - closes the current dataset.

**Plot Result** - plots the elements in a matrix versus one another, unless a different abscissa is selected. For example, when using this with the "spectra" matrix, the y vs. x are values in the matrix itself. In this case, the spectral abscissa is automatically selected (which then ignores the selected x value), but that can be changed by changing the abscissa value from "Spectral Abscissa" to "Column."

**Create Color Map** - creates a map of the matrix elements. This can only be done if the number of elements is the same as the x and y values.

**Info** - gives various info about the selected matrix.