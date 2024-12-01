# R-Test

1. Library Loading:

JavaScript
library(RStoolbox)
library(terra)
Use code with caution.

This code loads two libraries:
RStoolbox: This library provides tools for remote sensing data analysis in R, including spectral mixture analysis (SMA).
terra: This library is used for spatial data analysis and manipulation.
2. Endmember Selection:

JavaScript
# to perform a SMA, use a single endmember p
em <- data.frame(lsat [c(5294, 47916)])
rownames(em) <- c("forest", "water")
Use code with caution.

This code creates a data frame em containing two endmembers: "forest" and "water". Endmembers are pure spectral signatures of materials present in the image.
The endmembers are selected from the lsat image at specific pixel locations (5294 and 47916).
3. Spectral Mixture Analysis (SMA):

JavaScript
# unmix the lsat image
probs <- mesma (img = lsat, em = em)
Use code with caution.

This code performs spectral unmixing on the lsat image using the mesma function from the RStoolbox library.
The mesma function takes two arguments:
img: The input image (lsat in this case).
em: The endmember data frame created earlier.
The function estimates the fractional abundance of each endmember at each pixel of the image. The results are stored in the probs object.
4. Plotting the Results:

JavaScript
plot(probs)
Use code with caution.

This code plots the fractional abundance maps for each endmember ("forest" and "water"). The plots show the proportion of each endmember at each pixel location.
Purpose:

The purpose of this code is to perform a spectral mixture analysis on an image to estimate the abundance of two endmembers: "forest" and "water". The results of this analysis can be used to create maps showing the distribution of these land cover types.


![Capture](https://github.com/user-attachments/assets/fd5f09f3-f7f0-4c0e-8b48-235a8abf6291)
