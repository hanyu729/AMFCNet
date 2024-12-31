# AMFCNet: Attention-guided Multi-scale Feature Cascade Network for Underwater Fish Counting
# 1. Underwater Fish Counting
| ![Image 1](https://github.com/hanyu729/AMFCNet/raw/main/Figs/fig1a.png)  ![Image 2](https://github.com/hanyu729/AMFCNet/raw/main/Figs/fig1b.png) |
|----------------------------------------------------------------------------------------|
| *Figure 1(a): Non-underwater fish counting. The custom-built enclosed environment features clear water quality, uniform lighting, and consistent fish size.*        | *Figure 1(b): Underwater fish counting. The open environment is characterized by turbid water quality, uneven lighting, and varying fish sizes.*  |

As shown in Fig. 1, fish counting research can be classified into two categories based on different data collection locations: underwater and non-underwater fish counting. Non-underwater Fish Counting (NFC) methods typically involve deploying cameras above controlled environments, such as water tanks or buckets, to collect data. However, methods developed for such environments are often not directly applicable to open water or more complex conditions. NFC has high requirements on water clarity, lighting conditions, and water flow fluctuations, necessitating the use of specialized equipment. 
In contrast, Underwater Fish Counting (UFC) methods involve placing cameras directly in open environments, such as ponds or oceans, to collect data in natural underwater settings, making them more applicable to practical aquaculture. However, several challenges complicate UFC, including uneven light distribution, high levels of impurities, and the schooling behavior of fish at various life stages. To address these issues, we construct a new underwater fish dataset, UFCFish, and propose an Attention-guided Multi-scale Feature Cascade Network (AMFCNet) to enable precise underwater fish counting.

# 2. UFCFish dataset
The proposed UFCFish dataset contains 1,172 high-quality images, annotated with 152,596 points. Among them, 226 images show highly dense scenes, with more than 200 fish in each image. To standardize the benchmarking on UFCFish, the dataset is randomly divided into three non-overlapping subsets: train (703 images), validation (175 images), and test (294 images). Within each subset, the distribution of images across different density ranges closely matches the overall distribution.
| ![Image 3](https://github.com/hanyu729/AMFCNet/raw/main/Figs/fig2.png) |
|--------------------------------------------|
| *Figure 2: Example images from the proposed UFCFish dataset. From the left to the right column: samples with uneven lighting, samples with bubble impurities, samples from various water bodies, and samples with different fish densities.*       |

**Download links to our datasets will be publicly available soon!**

# 3. AMFCNet method
We propose an Attention-guided Multi-scale Feature Cascade Network (AMFCNet), which facilitates information flow and enhancement between different stages of the network through Multi-scale Attention Gate (MSAG) and Multi-scale Convolution Module (MSCM), and utilizes a Multi-head Supervision Fusion Strategy (MSFS) to generate high-quality density maps, enabling accurate underwater fish counting.

**For training/inference, please go to [here](https://github.com/hanyu729/AMFCNet/raw/main/AMFCNet/readme)**

# 4. Result
# 4.1 Comparison experiments.
| ![Image 4](https://github.com/hanyu729/AMFCNet/raw/main/Figs/fig3.png) |
|--------------------------------------------|
| *Figure 3: The visualization results of three scenarios are presented: columns 1-2 depict scenes with uneven lighting, columns 3-4 show scenes with impurity interference, and columns 5-6 represent scenes with different water bodies. The ground truth and predicted results are displayed in the bottom-left corner of each case.*       |

# 4.2 Varying densities experiments.
| ![Image 5](https://github.com/hanyu729/AMFCNet/raw/main/Figs/fig4.png) |
|--------------------------------------------|
| *Figure 4: Comparison of the prediction error fluctuations for different fish densities. The x-axis represents the index value (i) of the i-th image, while the y-axis indicates the prediction error for the i-th image. As observed from (a), the proposed method effectively addresses some challenging cases, with the overall error fluctuation stabilizing.*       |

# 4.3 Generalization experiments. 
| ![Image 6](https://github.com/hanyu729/AMFCNet/raw/main/Figs/fig5.png) |
|--------------------------------------------|
| *Figure 5: Qualitative comparison of various methods on the Orange Chromide dataset. Rows 1-2 illustrate examples of scale variation, while rows 3-4 demonstrate examples of noise interference.*       |

# 5. Conclusions
In summary, the proposed method has significant potential for practical applications in aquaculture (e.g., in marine ranching, pond farming) to assess fish growth conditions and adjust feeding strategies accordingly.
