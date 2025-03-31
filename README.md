# TEAM TOPICAL


### **👥 Team Members**

| Name | GitHub Handle | Contribution |
| ----- | ----- | ----- |
| Makayla Kienlen | @mkienlen | Built CNN, helped optimize model |
| Maria Sofia Sanchez | @marias65 | EDA, preprocessing and loading of dataset |
| Roma Solapurkar | @rsol1225 | Finetuned model |
| Ysabella Dela Cruz | @peeoke | Finetuned model |

---

## **🎯 Project Highlights**


* Built an image classification model with TensorFlow and Keras, to create a CNN, to identify skin conditions on a range of skin tones.
* Achieved an F1 score of \[insert score\] and a ranking of XX/73 on the final Kaggle Leaderboard
* Implemented label encoding, train-validation split, custom image data generators to optimize results within compute constraints

🔗 [Equitable AI for Dermatology | Kaggle Competition Page](https://www.kaggle.com/competitions/bttai-ajl-2025/overview)

---

## **👩🏽‍💻 Setup & Execution**

**Provide step-by-step instructions so someone else can run your code and reproduce your results. Depending on your setup, include:**

* To run the notebook, install the following: pip install pandas numpy scikit-learn tensorflow

* The dataset is availiable through the kaggle competitions
  
---

## **🏗️ Project Overview**

* Break Through Tech’s mission is to create an inclusive space for people from historically underrepresented backgrounds to gain experience in tech. This Kaggle competition aims to reduce bias in AI models aimed at identifying skin conditions. This competition allows for BTT students to use ML skills they have developed as a team in a competitive environment, with real world impact in creating more equality in the use of AI tools in healthcare.

* The goal of this Kaggle competition is to train a model that can classify 21 different skin conditions across diverse skin tones. 

* AI is transforming healthcare, yet dermatology AI tools often underperform for people with darker skin tones due to a lack of diverse training data. This can lead to diagnostic errors, delayed treatments, and health disparities for underserved communities. Our goal of creating an AI model that can fairly identify conditions on any skin tone shows that it is possible to overcome biases on AI models. Many industries benefit from AI tools, but it is important to make sure that any biases don’t impact customer experience. In the case of the healthcare industry, AI’s inability to correctly identify skin conditions on darker skin could cause health issues and people’s overall quality of life to worsen.

---

## **📊 Data Exploration**

* The dataset we used was provided by the Kaggle Competition. There are about 4500 images in this set, representing 21 skin conditions (eczema, acne-vulgaris, melanoma, etc). 

* To explore the data we first charted the distribution of the 21 classes, to see if there was an imbalance we had to address. We also looked over a few sample images from every class so we could get a feel for how similar the images were to each other. 

* During our preprocessing, we rotated all of the images to get more training data. 

* Some challenges we faced related to the data was that many of the conditions look similar to other conditions and that the same conditions can appear to look extremely different on different skin tones, so we were not sure how our model would work around this.


**Sample Dataset Images**

![](https://github.com/peeoke/TeamTopical/blob/main/2dc81d23b3c02663556832138db7d3d0.jpg)
![](https://github.com/peeoke/TeamTopical/blob/main/39db1b5308e58e1e486703dcb53b33ee.jpg)

First image shows an example of acne, second shows superficial spreading melanoma.

**Class Distribution Chart**

![](https://github.com/peeoke/TeamTopical/blob/main/LabelDistribution.jpeg)

---

## **🧠 Model Development**

Our model is a CNN that is specifically designed for image classficiation. Using TensorFlow and Keras, we created a sequential model in which the input layer is an image of size 128x128. There are then three convolutional layers that are all followed by a ma-pooling layer. The first layer used 32 filters with ReLU activation. The second and third layers use more filters. A flatten layer then converts the 3D tensor output into a 1D vector which is then passed to a dense layer with ReLU activation as well. The last layer output is a probability distribution over these classes.

The following is a visual representation of the layers in our model:
![alt text](https://github.com/peeoke/TeamTopical/blob/main/image.png)

---

## **📈 Results & Key Findings**

Performance metrics we used was our F-1 score which was also what our Kaggle Leaderboard score was based off of. Overall, our model has an F-1 score of 0.28933. 

---

## **🖼️ Impact Narrative**

**AJL challenge:**

As Dr. Randi mentioned in her challenge overview, “Through poetry, art, and storytelling, you can reach others who might not know enough to understand what’s happening with the machine learning model or data visualizations, but might still be heavily impacted by this kind of work.”
As you answer the questions below, consider using not only text, but also illustrations, annotated visualizations, poetry, or other creative techniques to make your work accessible to a wider audience.
Check out [this guide](https://drive.google.com/file/d/1kYKaVNR\_l7Abx2kebs3AdDi6TlPviC3q/view) from the Algorithmic Justice League for inspiration!

1. What steps did you take to address [model fairness](https://haas.berkeley.edu/wp-content/uploads/What-is-fairness_-EGAL2.pdf)? (e.g., leveraging data augmentation techniques to account for training dataset imbalances; using a validation set to assess model performance across different skin tones)

In order to ensure our model exhibited model fairness, we made sure to use the provided dataset of images to train our model. This dataset included various skin tones as well as various skin conditions, allowing us to train our model on a diverse dataset.


2. What broader impact could your work have? 

Our work could greatly assist the dermatology industry by allowing researchers and companies to be more inclusive in the work that they do. This competition as a whole focuses on broadening what skin types and colors can be processed by machine learning models created for the dermatology industry. By assisting these models and industries to be more inclusive, those who were underrepresented before can now benefit from the research done in dermatology.

---

## **🚀 Next Steps & Future Improvements**



Some limitations of our model include the limits that our own dataset is subjected to such as representation of certain skin conditions and skin colors. Skin conditions or skin colors that are not included in this dataset are not able to be predicted by our model. With more time and resources, our team would like to spend more time trying different types of models on the dataset. Some examples include decision trees, SVMs, random forest, and k-nearest neighbors. Additionally, we would also like to spend more time on output interpretation and visualization. By doing this, we would be able to better understand what our model is representing and how we could further improve our model. 

