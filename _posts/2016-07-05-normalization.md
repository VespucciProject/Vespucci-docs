---
layout: page
title: "Normalization"
category: pro
date: 2016-07-05 16:14:32
---

Normalization is a processing technique used in spectral analysis. Its primary purpose is in eliminating systematic variation between spectra. It can be implemented easily through Vespucci.

First, the desired dataset should be imported. Frequently, spectral data is baseline-corrected before normalization. After these steps, simply click the Processing tab and select Normalize/Standardize.

![Vespucci-NormalizeDialog](http://vespucciproject.org/Vespucci-docs/img/Normalize1.png)

Next, the desired form of normalization should be selected. A short description of each method is below.

![Vespucci-NormalizeSelect](http://vespucciproject.org/Vespucci-docs/img/Normalize2.png)

This should then cause all spectra to be normalized, as seen below.

![Vespucci-NormalizeShow](http://vespucciproject.org/Vespucci-docs/img/Normalize3.png)

### Normalization Methods ###
Vespucci supports 9 types of normalization: Min/Max, Unit Length, Unit Area, Z-score, Standard Normal Variate, Peak Intensity, Scale Spectra, Absolute Value, and Mean Center.

**Min/Max**
Min/max normalization transforms each spectrum so that the highest point in a spectrum as 1, and the lowest as 0, to result in a range from 0-1. This is also known as [feature scaling](https://en.wikipedia.org/wiki/Feature_scaling).

**Unit Length**
Unit length normalization divides each point of each spectrum by the 2-norm of that spectrum. This transforms each spectrum so that the spectrum vector has unit magnitude.

**Unit Area**
Unit area normalization divides each point of each spectrum by the 1-norm of that spectrum. Unit area normalization transforms each spectrum so that the spectrum vector has unit area, resulting in the sum of all values of the spectrum being equal to 1.

**Z-score**
Z-score normalization replaces each value of each spectrum with its [Z-score](https://en.wikipedia.org/wiki/Standard_score), calculated from the standard deviation and mean of each spectrum. This is also referred to as "standardization" and results in a mean of 0 and standard deviation of 1 for each spectrum.

**Standard Normal Variate**
Standard normal variate normalization replaces each value of each spectrum with its Z-score, calcualted from the standard deviation and mean of every value in the spectra matrix at that spectral abscissa value. This results in a mean of 0 and standard deviation of 1 for each spectral abscissa value. This is often used for multivariate analysis. Like mean centering, this affects the interpretability of individual spectra because their values are now weighted based on their deviations from the centroid of the spectra matrix.

**Peak Intensity**
Peak intensity normalization scales each spectrum by the maximum value of that spectrum within a user-specified spectral abscissa range. 

**Scale Spectra**
The scale spectra option allows a user to multiply a spectra by any desired value: 100, -1, etc. Scaling by -1 reflects each spectrum about the spectral abscissa, making negative "valleys" appear as positive "peaks".

**Absolute Value**
Absolute value replaces each point of the spectra matrix with its absolute value.

**Mean Center**
In mean centering, the average spectrum of a dataset is calculated, then subtracted from each individual spectra. This results in a mean value of 0 for each spectral abscissa value. Note that Vespucci will automatically mean-center all data used in principal component analysis. Like standard normal variate normalization (which combines mean centering with scaling by the standard deviation), this method affects the interpretability of the individual spectra because their values are now weighted based on their deviation from the centroid of the spectra matrix.
