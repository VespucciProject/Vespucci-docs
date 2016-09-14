---
layout: default
title: "Vespucci User Manual"
---
### Vespucci v1.0.0 User Manual
Select one of the topics on the left to learn how to use Vespucci.

Vespucci is a tool optimized for spectral analysis. An example of this will be shown below. You can also select any of the topics on the left to go to a more detailed description of that specifically.

### Example
In this example, Raman spectral data for a biological cell will be examined to obtain information about the studied sample.

Vero 76 African green monkey kidney cells were used. In the procedure, they were incubated with silver nanoparticles for 24 hours. The nanoparticles were then uptaken by the cell. This allowed the [SERS effect](https://en.wikipedia.org/wiki/Surface-enhanced_Raman_spectroscopy) to be used in the Raman analysis. After this, Raman spectroscopy was performed on the cells, more specifically a Raman "map." A Raman map moves over a two-dimensional area to record point spectra every 1 µm (or whatever increment is chosen, based on the capabilities of the machine).

Take a look at the following image, taken with 140X magnification on a microscope attached to a Raman instrument.

![Example-Raman_Map](http://vespucciproject.org/Vespucci-docs/img/Example1_Raman_Map.png)

It's quite dark, and the cell features can't be seen at all. However, using Vespucci we can get a clear picture of where things are.

The data is first imported into Vespucci.

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/ImportFile1.png)

In the following image, notice that the "swap x and y" option is selected. This is because the way the instrument records the positional mapping data (x first, or y first) and the way that Vespucci interprets that data are reversed. The way it is stored depends on the software used for the Raman analysis--thus different software might not need this option checked. To check this, you might perform a rectangular map, for instance 2x1. Then, after importing into Vespucci, you can see if the horizontal and vertical points line up correctly.

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example2_Dataset_Import.png)

After this, the spectral data is filtered and normalized. Filtering removes sharp spikes which occasionally occur during spectral aquisition, and normalization can remove systemic variation between data.

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example3_Filter.png)

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example4_Filter_Select.png)

In this case, a Median filter was used, which for each point on a spectra takes a user-specified number of points around and including the point of interest, and makes that the new value.

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example4_Normalize.png)

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example5_Normalize_Select.png)

Unit area normalization was used, which transforms the spectra so that it has unit area.

After this, the multivariate analysis was performed, more specifically k-Means clustering. This analysis technique randomly picks a user-defined number of spectra and defines these as "clusters."  Next, each spectra is compared to the centroid (or "mean" psudo-spectra of all spectra within a cluster) of each cluster, and added to the cluster it is closest to. The centroid of that cluster is then updated.

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example6_kMeans.png)

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example7_kMeans_Select.png)

After the analysis is performed, one can both look at the centroids and look at the 2-D map. Both are simple. To look at the centroids, one first navigates to the k-Means analysis results, then selects the "Centroids" matrix. After doing so, one can plot them by selecting the plot icon on the toolbar. The proper centroid is chosen by changing the y axis (in the image below the 1st centroid is selected). The resulting image can be exported--note that this is an image, not the spectra itself. That can be exported through selecting the matrix and selecting File>Export Matrix.

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example8_Plot_Centroids.png)

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example9_Plot_Centroids_Select.png)

The 2-D map can be viewed as well. It must first be created by selecting the Assignments matrix, then pressing the "Create Color Map" icon on the toolbar. The desired color gradient can be selected on the resulting dialog box; the default setting is designed to make the color of each cluster as visually distinct as possible (by automatically picking the colors based on the number of clusters). After this is done, the map is created, and can be opened by double-cklicking on it in the dataset navigator.

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example10_Map_Assignments.png)

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example11_Map_Assignments_Select.png)

![Vespucci-ImportFileSelect](http://vespucciproject.org/Vespucci-docs/img/Example12_Color_Map_kMeans.png)

Each color on the above image coresponds to a different cluster, which the spectrum at that point is most similar to. You can move around on the map using the crosshairs--moving them with the arrow keys or WASD on a keyboard creates a spectrum in the plot viewer. Please note that unless the "Hold" option in the plot viewer is checked, this will create a NEW tab each time the crosshairs move, potentially resulting in dozens of tabs.

By viewing the map above, we can see that there are different "regions" in the sample, clustered in broad shapes.


It can be seen that by using the above techniques (as well as many others), Vespucci can give important information, spatial or otherwise, about a sample.
