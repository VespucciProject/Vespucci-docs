---
layout: page
title: "Normalization"
category: pro
date: 2016-07-05 16:14:32
---

Normalization is a processing technique used in spectral analysis. Its primary purpose is in eliminating systematic variation between spectra. It can be implemented easily through Vespucci.

First, the desired dataset should be imported. Frequently, spectral data is baseline-corrected before normalization. After these steps, simply click the Processing tab and select Normalize/Standardize.

![Vespucci-NormalizeDialog](Vespucci-docs/img/Normalize1.png)

Next, the desired form of normalization should be selected. A short description of each method is below.

![Vespucci-NormalizeSelect](Vespucci-docs/img/Normalize2.png)

This should then cause all spectra to be normalized, as seen below.

![Vespucci-NormalizeShow](Vespucci-docs/img/Normalize3.png)



### Normalization Methods ###

Vespucci supports 9 types of normalization: Min/Max, Unit Length, Unit Area, Z-score, Standard Normal Variate, Peak Intensity, Scale Spectra, Absolute Value, and Mean Center.

**Min/Max**

Min/max normalization simply defines the highest point in a spectrum as 1, and the lowest as 0, to result in a range from 0-1.

**Unit Length**

Unit length normalization takes the magnitude of the vector and sets it equal to 1.

**Unit Area**

Unit area normalization defines the area under the sprctrum as 1.

**Z-score**

Z-score normalization takes the mean value of a spectrum and compares every point to that and the standard deviation of all points, creating a scale based on standard deviation. It also normalizes spectra by columns.

**Standard Normal Variate**

Standard Normal Variate is much like Z-score normalization, except that it normalizes spectra by rows, and it takes the mean value and standard deviation of all points at a particular wavenumber in *all* spectra.

**Peak Intensity**

Peak intensity normalization takes a user-defined wavenumber range and makes the height of any peak in that range 1.

**Scale Spectra**

The scale spectra option allows a user to multiply a spectra by any desired value: 100, -1, etc. Scaling by -1 allows one to invert negative peaks.

**Absolute Value**

Absolute value takes the absolute value of each point on each spectrum.

**Mean Center**

In mean centering, the average spectrum of a dataset is calculated, then subtracted from each individual spectra.