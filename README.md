Developed an AI model for tongue image analysis using  deep learning techniques (CNN)

"I developed a Convolutional Neural Network (CNN) model to classify tongue images based on principles from Traditional Chinese Medicine (TCM) and Ayurveda.”

"Tongue diagnosis is very fascinating and traditional method used in TCM and Ayurveda to assess health by examining the tongue's appearance . Tongue is  an indicator of our body   that can reveal imbalances like excess heat, stress, sugr or deficiencies in vitamins. However, manual assessment can be subjective and time-consuming.”

## TECHNICAL

- "I collected a diverse **`*DATASET*`** of tongue images and ensured high quality from different platform. Each image was labeled according to the specific diagnostic categories used in TCM and Ayurveda. and verified by professionals"
- specially in 7 different classes that are
- NON-tongue - from coco
- healthy tongue - kaggle
- ayurveda 3 - from  IEEE Dataset
- fiss , diab —> Aiims Delhi

**`Pre-Processing`**

—> Converting all images to jpeg format  

*image = tf.image.decode_jpeg(image_contents, channels=3)*

—>and image size 256,256 , channel 3

resizing dataset using `rescaling` to 1/255

data `augmentation` 

from keras sequintial library

`Model BUilding`

splitting in train test and validation —> 

```python
from sklearn.model_selection import train_test_split

```

"I used a Convolutional Neural Network `*(CNN)*` due to its effectiveness in image classification tasks.

Input Shape-➖ `image size channel , batch size and classes`

Model Architecture:-: The architecture includes several convolutional layers to extract features from the images:

***Conv2D Layers:*** These 64 layers apply filters to learn different features from the images, with increasing depth and complexity.
***MaxPooling2D Layers:*** These layers reduce the size of the feature maps while retaining the most important information.
***Flattening and Dense Layers*:** The output is flattened and passed through dense layers to learn higher-level representations and make final predictions."

`history = model.fit(
train_images,
train_labels,
epochs=10,
batch_size=32,
validation_data=(val_images, val_labels) validation_data` allows monitoring the model's performance on a separate validation set to assess how well it generalizes.
`)`

**Evaluation Metrics:** "You use `model.evaluate()` to measure the model’s performance on test data, which provides an indication of how well the model generalizes to unseen data."

**Deployment:** Finally, the trained model can be deployed for practical use, such as assisting in health diagnostics based on tongue images."
