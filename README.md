# CFHT_2023

Abstract:
Used a Convolutional Neural Network to detect clouds on Mauna Kea using Canada France Hawaii Telescope’s (CFHT) All Sky Infrared and Visible Analyzer (ASIVA). Two models were constructed: a full-sky image classifier and a heatmap generator based on different size pixel kernels. The full-sky classifier was able to determine clear skies with 100% accuracy (0% false positive rate) and cloudy skies with 96% accuracy (4% false negative rate). The heatmap generator model used a machine learning network on a small kernel which it passed over an input image to determine the likelihood of cloud coverage at each location. Data cleaning was required to yield significant results due to dynamic range limitations of the sensor causing significant differences between clear and cloudy images. Different batch sizes were compared to test model convergence, ROC performance, and overall effectiveness. Smaller batch sizes were found to be more effective with a batch size of 32 yielding an AUC of 0.987. Cloud coverage percentage was determined by comparing each kernel’s prediction value against a determined threshold constant and dividing the number of kernels classified as cloudy by the total number of kernels. Overall, the heatmap model was found to provide significantly more data than the current system on cloud coverage over Mauna Kea. Cloud coverage percentage is a metric not currently available for continuous image acquisitions over Mauna Kea. Additionally, the heatmap approach provides data on cloud coverage in specific sky regions, allowing for much more accurate observations of cloud activity in regions of interest.





Source code at:
https://github.com/ijustdontgitit/asiva_clouds
