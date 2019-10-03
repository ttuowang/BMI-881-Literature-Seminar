BMI 899
=======

Paper Summary Week IV
---------------------

**Tuo Wang**

Assessment of Deep Learning Using Nonimaging Information and Sequential
Medical Records to Develop a Prediction Model for Nonmelanoma Skin
Cancer

In this paper, the researchers constructed a deep learning convolutional
neural network (CNN) and then applied CNN to non-imaging and sequential
medical records to predict nonmelanoma skin cancer (NMSC). The data was
from the Taiwan National Health Insurance Research Database and
contained only Asian patients. The study converted each individual’s
medical information into an image-like matrix with medical events and
sequential medical information. The study used the area under the ROC
curve (AUROC), sensitivity and specificity as the metric to evaluate the
performance of CNN. Further, to measure which features will affect the
performance, the study constructed many sub-CNN models, for example, CNN
model with only diagnosis information, CNN model with only medication,
CNN model without age, etc. Then, the study measured the reduction in
AUROC between the sub-CNN models and the complete model, which include
all the features. The results showed the model with both diagnosis and
medication information performs the best. The results also showed that
age didn’t have strong affect the AUROC even though the average age in
the control group is approximately 20 years old younger than the NMSC
group. Finally, the researchers compared the performance of the CNN with
the results of other studies and concluded that their results are
relatively better.

At first glance at the title of this paper, I feel very skeptical that
one can apply CNN on medical records because CNN uses a filter kernel
matrix to capture the local correlation between covariates. After
detailed reading through the paper, I’m amazed at how the researchers
convert the medical record into an image-like matrix with sequential
medical records. This makes sense. Usually, when a doctor asks a patient
to have certain medicine, it will last for a while, for example, a
month. By looking at the performance, the mean AUROC, sensitivity, and
specificity are good. Precision is around 50%. The data is kind of
unbalance. The ratio of NMSC and controls without cancer is 1:4, which
means that if a classifier classifies all the subjects to no cancer, the
accuracy will be 80%. However, AUROC is a robust metric even though the
data is unbalanced so overall the performance of CNN is good. The study
selects the optimal cutoff risk score threshold based on maximizing both
sensitivity and specificity, but I think in the case of cancer,
sensitivity plays a more important role than specificity. We don’t want
to mispredict a patient with potential cancer risk to no risk.
