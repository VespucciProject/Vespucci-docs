---
layout: page
title: "Importing Data"
category: dat
date: 2016-07-05 16:13:33
---


Importing data into Vespucci is a simple process. One must first select the File option to import an external dataset.

![Vespucci-ImportFileSelect](Vespucci-docs/img/ImportFile1.png)

Doing this opens a new dialog box. The file of interest can be searched for by selecting Browse, then selected by moving through the standard folder structure to the location and file of interest. Vespucci currently supports .txt file types as a single dataset, and .txt, .csv, and .dat file types for multiple point spectra.

Once this is complete, the selected file should be visible in the "browse" window. Depending on how the information is stored in the file, the "Swap x and y?" choice should be selected. Vespucci normally expects the x axis first in a dataset, but this can be changed.

![Vespucci-ImportFileDialog](Vespucci-docs/img/ImportFile3.png)

Additionally, the "long" or "wide" data formats can be selected. Long data separates all values into columns, such that all abscissa points, with their corresponding spectra values, would be on individual rows. Wide text puts all abscissa points first, with the spectra values later. This is slightly more complex when a "map" (spectral data taken over a 2D grid) is involved. 

Once this is finished, various options such as axis units or description can be changed as desired. Once finished, press "OK."

![Vespucci-ImportFileSuccess](Vespucci-docs/img/ImportFile4.png)

This should open the dataset in Vespucci, visible in the central window, for further use.