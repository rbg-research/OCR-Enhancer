# OCR-Enhancer

# Performing Text Segmentation to Improve OCR on Multi Scene Text

**Abstract**:Optical Character Recognition (OCR) is a revolutionary technique that aids machines in retrieving textual content from images to perform further analysis. However, OCR has its limitations, especially when dealing with degraded or low-quality images, which can impact the overall reliability of the text recognition process. Thus, the system’s accuracy is contingent upon the quality of the input (digital or handwritten documents). Efforts to modify the text detection and text recognition modules in existing OCRs fail to work in complex dynamic environments due to the complexity of the background information of the input data. Thus, a new first-of-its-kind annotated dataset called OCR-SBT for digital text segmentation is proposed in this work, along with a novel preprocessing pipeline using deep learning that performs text retrieval from images having varying and complex backgrounds using binary semantic segmentation. With quantitative metrics such as the DICE coefficient as high as 99.56%, the qualitative performance improvement of OCR has also been validated on real-world test samples containing varying contextual information to validate the model’s efficacy. Ablation experiments are also performed to determine the importance of super-resolution of input images using Stable Diffusion and ESRGAN. This work will help the research community to improve OCR for several real-world applications by alleviating the problems related to background contextual information obfuscating the text recognition module.

The Best Paper award-winning paper is submitted at the 5th International Conference on Artificial Intelligence and Speech Technology (AIST-2023)

## Dataset

The OCR-SBT Dataset This research uses a painstakingly selected dataset of synthetic text pictures to perform OCR with Scene Binarized Text (OCR-SBT). The raw images on which binarization had to be performed were taken from the SynthTiger Dataset library, which holds an astounding 10.7 million images with a single word. Thus, it includes various changes and variants to thoroughly test and assess our suggested OCR-enhancing strategy. With an emphasis on English, the subset of 1,684 text images on which binarization was performed reflects a cross-section of this sizable dataset.

![Sample images and binary segmentation masks of the dataset introduced](images/dataset.jpg)

## Proposed Methodology

The pipeline begins with creating binary segmentation masks using the color k-means technique to separate the text foreground from the background. Then, UNet and UNet3+, two different segmentation architectures, are used to train reliable binary segmentation models that can effectively isolate text sections. The pipeline also contains image super-resolution algorithms - the ESRGAN and Stable Diffusion methods to improve the quality of the raw text pictures for further enhancement. The study demonstrates significant gains in OCR performance using this integrated approach, especially for text images with complex backgrounds and varied properties.

![Proposed approach to perform text segmentation and OCR](images/workflow.jpg)
