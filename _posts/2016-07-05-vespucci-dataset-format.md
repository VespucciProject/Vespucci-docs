---
layout: page
title: "Vespucci Dataset Format"
category: dat
date: 2016-07-05 16:14:07
---
Vespucci uses the standard [HDF5 file format](https://www.hdfgroup.org/HDF5/) for saving datasets, and can import HDF5 formats saved by other software. HDF5 files saved by Vespucci store matrices as row-major C-style arrays, which are transposed compared to how they are stored in the program.

The Vespucci dataset format is a subset of HDF5 that is structured like this:
The "dataset" is the root of the file.
The core matrices ("Spectra", "Spectral Abscissa", "x", "y") belong to the root of the file.
Matrices that are generated from analysis are each stored as groups. These groups contain arrays corresponding to matrices in Vespucci.

The hierarchy of the format mirrors that displayed in the Vespucci main window.

To save an HDF5 that can be opened by Vespucci you must have datasets named "Spectra" and "Spectral Abscissa" belonging to the root of the file. Your file must be only two groups deep. Datasets belonging to the root of the file that are not named one of the four reserved names will be ignored. All matrices will be imported as row-major. "Spectral Abscissa" must have only one row and the same number of columns as "Spectra".

