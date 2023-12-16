# Image-Enhancement-Image-Histogram
Image enhancement is basically improving the digital image quality. Image histogram is helpful in image enhancement
Image enhancement is the process of adjusting digital images so that the results are more suitable for display or further image analysis. Image enhancement can be done by Histogram equalization. Histogram equalization is a technique for adjusting image intensities to enhance contrast.Image enhancement is basically improving the digital image quality. Image histogram is helpful in image enhancement. The histogram in the context of image processing is the operation by which the occurrences of each intensity value in the image is shown and Histogram equalization is the technique by which the dynamic range of the histogram of an image is increased.

code explaination

This code demonstrates how to calculate and visualize the histogram of grayscale and color images using OpenCV and matplotlib.

Part 1: Grayscale Image Histogram

Load Image: Reads the image "ambani.jpg" in grayscale format using cv2.imread and stores it in gray_img.
Display Image: Shows the grayscale image in a window titled "RICHEST MAN" using cv2.imshow.
Calculate Histogram: Uses cv2.calcHist to calculate the histogram of the grayscale image.
It specifies the image (gray_img) as the input, the channel index (0 for grayscale), no mask, 256 bins, and the intensity range (0-255).
The result is stored in hist.
Plot Histogram: Uses plt.hist to plot the histogram of the image.
It uses the flattened array of pixel values (gray_img.ravel()) and 256 bins with the same intensity range.
Sets the title to "Histogram for gray scale picture".
Displays the plot using plt.show.
Exit Loop: Checks for the ESC key press (27) and exits the loop if pressed, closing all windows with cv2.destroyAllWindows.
Part 2: Color Image Histogram

Load Image: Reads the image "tajhotel.jpg" in color format using cv2.imread and stores it in img.
The flag "-1" indicates reading the image in its original format with all channels.
Display Image: Shows the original color image in a window titled "GoldenGate" using cv2.imshow.
Calculate Histograms: Loops through the three color channels (blue, green, and red) using enumerate.
For each channel, uses cv2.calcHist to calculate the histogram similar to the grayscale case.
Stores the results in separate variables (histr).
Plot Histograms: Uses plt.plot to plot the histograms of each channel on the same plot.
Sets different colors for each channel using the color variable.
Sets the x-axis limits to the intensity range (0-255).
Sets the title to "Histogram for color scale picture".
Displays the combined plot using plt.show.
Exit Loop: Similar to Part 1, checks for ESC key press and exits the loop, closing all windows.
Overall, this code provides a basic example of how to analyze the distribution of pixel intensities in both grayscale and color images using histograms. It can be helpful for understanding image features and developing image processing algorithms.
