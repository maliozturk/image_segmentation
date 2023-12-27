# Introduction
## Background
Image segmentation plays a crucial role in various applications, particularly in decision-oriented contexts. This project draws inspiration from a research paper titled "Image Segmentation using K-means Clustering Algorithm and Subtractive Clustering Algorithm." The background emphasizes the significance of clustering methods, specifically the K-means and Subtractive Clustering algorithms, in achieving accurate image segmentation.

## Objectives
The primary objective of this project is to implement and evaluate an advanced image segmentation algorithm based on the methodologies presented in the referenced paper. Specific goals include understanding the clustering techniques, applying partial stretching enhancement to improve image quality, and combining Subtractive Clustering with K-means for segmentation. The project also aims to assess the effectiveness of the proposed algorithm against other segmentation techniques.

## Methodology
The methodology involves a detailed examination and implementation of the K-means and Subtractive Clustering algorithms as described in the referenced paper. The process includes initial partial stretching enhancement, generation of initial centers using Subtractive Clustering, and subsequent application of K-means for image segmentation.

# Experimental Evaluation
## Dataset and Model Architecture
The dataset architecture utilized in the project consists of brain MRI images obtained from Kaggle. These images serve as the basis for implementing and testing the proposed image segmentation algorithm. This dataset contains brain MR images. The images were obtained from The Cancer Imaging Archive (TCIA). Each image's size is 256x256, and the entire set of 110 patients was split into 22 non-overlapping subsets of 5 patients each. I have selected one of the subsets, which contained 20 images.

## Accomplishments
Accomplishments in the project encompass the successful implementation of the proposed algorithm, the selection of a suitable brain MRI dataset, and the extension of the project scope by incorporating the Gaussian Mixture algorithm.

### Implementation Steps & Things Done After Progress Report
Implementation steps involve selecting an image, applying partial contrast stretching, calculating potentials, modifying the K-means algorithm, applying the Gaussian Mixture technique, plotting results, and evaluating performance metrics. Detailed steps are as following:

1. First, we selected an image from the dataset.
2. Then we stretched the image using the partial contrast stretching technique.
3. We calculated potential for each pixel and updated potentials until finding K number of centroids.
4. We modified the default K-means algorithm for initial centroids other than random initial centroids and applied it to both cases.
5. We applied the Gaussian Mixture technique to the image in addition to K-means with initial random centroids and potential centroids techniques.
6. We plotted the results and compared them with each other.
7. We calculated RMSE and PSNR values as given in the paper between the segmented image and the original image.

And after the progress report, we've done the followings:

- Paper was fully implemented.
- Dataset has been selected.
- Project report and final presentations have been prepared.
- Gaussian mixture algorithm has been added in addition to the techniques used in the paper.

## Difficulties
Challenges encountered during the project include understanding the potential calculation in the Subtractive Clustering Algorithm, the absence of previous implementations, dataset selection, computational challenges in potential calculation, and discrepancies in achieving results similar to those in the paper. In summary, difficulties were:

- Finding the potential of each pixel (Subtractive Clustering Algorithm) was challenging to understand. Implemented the mountain technique first to comprehend the method proposed in the paper.
- Despite the paper having numerous citations, it hadn't been implemented anywhere before this project's work. The implementation process consumed a significant amount of time.
- No dataset was provided in the paper, requiring the search and selection of a suitable dataset from the web for applying image segmentation. Brain MRI images from Kaggle were chosen for segmentation to align with the techniques given in the paper.
- The proposed potential finding formula uses data points as candidates for cluster centers, and the computation of this method is proportional to the problem size. For larger images, computation time increases. To address this, the images were resized from 256x256 to 128x128 before applying the technique.
- Couldn't achieve similar results as shared in the paper.

## Results and Analysis
Table 1 displays the findings of experiments conducted. As illustrated in the table, results obtained from the proposed algorithm, default K-means algorithm, and Gaussian Mixture technique are presented and analyzed. Observations highlight performance disparities and potential areas for optimization.

| Algorithm            | Average RMSE | Average PSNR |
|----------------------|--------------|--------------|
| Proposed Algorithm   | 7.85         | 18.14        |
| Default KMeans       | 6.25         | 27.96        |
| Gaussian Mixture     | 6.63         | 25.60        |

- The proposed algorithm exhibits a higher RMSE and lower PSNR compared to the default K-means algorithm, indicating potential room for improvement.
- The Gaussian Mixture technique performs competitively but falls between the proposed algorithm and the default K-means algorithm in terms of both RMSE and PSNR.

An example output will be shared in figure 1. You can find the source codes for this project on GitHub at: [https://github.com/maliozturk/image_segmentation](https://github.com/maliozturk/image_segmentation).

![A segmented image with the implemented algorithms.](results_cmp730.png)

# Conclusion
The project has provided valuable insights into the performance of the implemented image segmentation algorithm. While the proposed algorithm demonstrated higher RMSE and lower PSNR compared to the default K-means algorithm, these findings suggest areas for refinement and enhancement. The competitive performance of the Gaussian Mixture technique adds complexity to the comparison, falling between the proposed algorithm and the default K-means algorithm in terms of both RMSE and PSNR.

The difficulties encountered during the project, including challenges in understanding the Subtractive Clustering Algorithm, the absence of previous implementations, dataset selection, and computational constraints, underscore the complexity of implementing advanced segmentation techniques.

In conclusion, the project lays the foundation for future optimizations and refinements to the image segmentation algorithm. The insights gained contribute to the broader field of image processing and segmentation, opening avenues for further research and improvement. Moving forward, further analysis and experiments will be conducted to gain deeper insights into the performance differences between the one proposed in the paper and the one we get in the end. Additionally,
