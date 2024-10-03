# ISIC Challenge 2024

In this competition, an image-based algorithm was developed to identify histologically confirmed skin cancer cases with single-lesion crops from 3D total body photos (TBP). The image quality resembles close-up smartphone photos, which are regularly submitted for telehealth purposes. The binary classification algorithm could be used in settings without access to specialized care and improve triage for early skin cancer detection.

<img src="https://github.com/cgrundman/isic_challenge/blob/main/isic_1.png" width="400" />

## Description

Skin cancer can be deadly if not caught early, but many populations lack specialized dermatologic care. Over the past several years, dermoscopy-based AI algorithms have been shown to benefit clinicians in diagnosing melanoma, basal cell, and squamous cell carcinoma. However, determining which individuals should see a clinician in the first place has great potential impact. Triaging applications have a significant potential to benefit underserved populations and improve early skin cancer detection, the key factor in long-term patient outcomes.

Dermatoscope images reveal morphologic features not visible to the naked eye, but these images are typically only captured in dermatology clinics. Algorithms that benefit people in primary care or non-clinical settings must be adept to evaluating lower quality images. This competition leverages 3D TBP to present a novel dataset of every single lesion from thousands of patients across three continents with images resembling cell phone photos.

This competition challenges you to develop AI algorithms that differentiate histologically-confirmed malignant skin lesions from benign lesions on a patient. Your work will help to improve early diagnosis and disease prognosis by extending the benefits of automated skin cancer detection to a broader population and settings.

## Dataset Description
What should I expect the data format to be?
The dataset consists of diagnostically labelled images with additional metadata. The images are JPEGs. The associated .csv file contains a binary diagnostic label (target), potential input variables (e.g. age_approx, sex, anatom_site_general, etc.), and additional attributes (e.g. image source and precise diagnosis).

What am I predicting?
In this challenge you are differentiating benign from malignant cases. For each image (isic_id) you are assigning the probability (target) ranging [0, 1] that the case is malignant.

### The SLICE-3D dataset - skin lesion image crops extracted from 3D TBP for skin cancer detection

To mimic non-dermoscopic images, this competition uses standardized cropped lesion-images of lesions from 3D Total Body Photography (TBP). Vectra WB360, a 3D TBP product from Canfield Scientific, captures the complete visible cutaneous surface area in one macro-quality resolution tomographic image. An AI-based software then identifies individual lesions on a given 3D capture. This allows for the image capture and identification of all lesions on a patient, which are exported as individual 15x15 mm field-of-view cropped photos. The dataset contains every lesion from a subset of thousands of patients seen between the years 2015 and 2024 across nine institutions and three continents.

The following are examples from the training set. 'Strongly-labelled tiles' are those whose labels were derived through histopathology assessment. 'Weak-labelled tiles' are those who were not biopsied and were considered 'benign' by a doctor.

<img src="https://github.com/cgrundman/isic_challenge/blob/main/isic_3.png" />

### Dataset Citation

International Skin Imaging Collaboration. SLICE-3D 2024 Challenge Dataset. International Skin Imaging Collaboration https://doi.org/10.34970/2024-slice-3d (2024).

Creative Commons Attribution-Non Commercial 4.0 International License.

The dataset was generated by the International Skin Imaging Collaboration (ISIC) and images are from the following sources: Hospital Clínic de Barcelona, Memorial Sloan Kettering Cancer Center, Hospital of Basel, FNQH Cairns, The University of Queensland, Melanoma Institute Australia, Monash University and Alfred Health, University of Athens Medical School, and Medical University of Vienna.

## Image Modality

### 3D Whole Body Photography
Designed specifically for dermatology, the VECTRA WB360 whole body 3D imaging system captures the entire skin surface in macro quality resolution with a single capture by processing 92 camera images (46 bi-camera positions).

### Tiles
The location of each lesion on the patient is detected automatically and exported as individual 15x15 mm field-of-view cropped images. The test set and training sets are comprised of tiles. Teams are permitted to use other public datasets for developing algorithms.

### Dermoscopy
Dermoscopy refers to the examination of the skin using skin surface microscopy. Dermoscopy requires a high quality magnifying lens and a powerful lighting system (a dermatoscope), which illuminate morphologic features not otherwise visible to the naked eye. Large dermoscopy datasets are available on ISIC.

<img src="https://github.com/cgrundman/isic_challenge/blob/main/isic_2.jpg" />

Read more about the competition [here](https://www.kaggle.com/competitions/isic-2024-challenge).
