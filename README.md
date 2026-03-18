# Machine-Learning-Diagnosis-of-Diabetic-Eye-Disease-
## Developed CNN and SVM models to classify Retinopathy using binary, scalar and image data. Achieved classification accuracy of 92.5% using Optuna tuning and data augmentation techniques.

Diabetic Macular Edema (DME) and Diabetic Retinopathy (DR) result from damage to the
eye caused by the high blood sugar levels of diabetic patients. These diseases are prevalent among
diabetics and can cause major visual complications with DR being a leading cause of blindness.
Approximately 70% of patients with type 1 diabetes will develop DR and 25% of diabetes patients
may develop DME. Accurate diagnosis is imperative in order to determine suitable treatment specific
to the disease. AI models are increasingly being used in the medical field due to their ability to
analyse large volumes of data and detect subtle patterns missed by human analysis. They offer the
key to timely and accurate diagnosis to mitigate symptoms and alleviate pressure on understaffed
healthcare institutions.

The objective of this project was to develop, evaluate, and optimise a range of supervised
machine learning models capable of reliably distinguishing between DR and DME using a
combination of numerical clinical data, binary biomarkers, and retinal OCT images.

I applied dimensionality reduction (PCA, t-SNE) to the data to explore class separability in
different combinations of the numerical and binary data. I trained and tuned two types of supervised
models: SVM and CNN. The simpler SVM model was optimally tuned using an RBF kernel and applied
to the numerical and binary data. For the image data, I designed and optimised CNN architectures,
applied hyperparameter tuning with Optuna, introduced data augmentation techniques (rotation,
scaling, flipping, noise) and evaluated transfer learning with a pre-trained VGG16 model to improve
generalisation.

The SVM achieved a peak accuracy of 92.5%, significantly outperforming the initial CNN
which achieved a peak accuracy of 85% when utilising an optimised set of augmentation techniques.
My analysis determined that the SVM excelled because the pre-processed numerical biomarkers
were more information dense and manageable for a small dataset, whereas the CNN was data
starved and prone to overfitting on the complex, high-dimensional OCT images. Data augmentation
mitigated overfitting, increasing the accuracy of the CNN from 79% to 85%. However, there was still
insufficient unique data in the complex OCT images for the CNN to learn features as effectively as the
SVM could process the information dense clinical labels and biomarkers.
