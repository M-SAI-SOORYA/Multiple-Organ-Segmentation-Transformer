# Multiple-Organ-Segmnetation-Transformer
So yeah, we as a team of 6 members developed a mobile application that can automatically segment multiple organs from abdominal CT scans using Generative AI. This means the app takes a CT scan as input and highlights different organs separately, making it useful for medical diagnosis and analysis. The project combines deep learning and Transformers, mobile development, and cloud computing to create a seamless end-to-end solution.

How It Works
User Interaction

Step 1: Users upload a CT scan image in the app.
Step 2:The AI model processes the image and segments different organs.
Step 3:The result is displayed in the app, showing which organ is where.
Technology Stack

Front-end: Built using Flutter for a smooth mobile experience.
Backend: Flask API handles requests and runs the deep learning model.
Deep Learning: TensorFlow framework is used to train the model.
Cloud Deployment: AWS cloud services help deploy and run the model efficiently.


Dataset Used

The model is trained on the Synapse multi-organ segmentation dataset, which contains abdominal CT scan images labeled with different organs.
AI Model Used
Three different models were explored for segmentation:

UNETR (Main Model) – Uses a Vision Transformer as the encoder and a CNN-based decoder. It captures global features efficiently, making it highly accurate.

UNET – A classic segmentation model with an encoder-decoder structure. Works well but is not as powerful as transformers.

DETR (Detection Transformer) – A transformer-based model, but primarily for object detection rather than segmentation.

Among these, UNETR was chosen as the primary model due to its superior performance in segmenting complex structures.

Training the Model
The model was trained using 4720 images, split into:
60% for training

20% for testing

20% for validation

Different hardware setups were tested:
CPU: Too slow, taking 6+ hours per epoch.

GPU: Faster (~200 seconds per epoch), but limited by memory.

TPU: The fastest (~100 seconds per epoch), allowing larger batch sizes.

Finally!
A fully functional mobile application where users can upload CT scan images of abdomen and get segmented results in real time.
The app is deployed on AWS, making it accessible remotely.
The segmentation accuracy is high, making it useful for medical professionals.


Impact
This project can assist radiologists and healthcare professionals in faster and more accurate medical image analysis, reducing manual efforts in segmentation. It also has the potential to be integrated into hospital systems for automated diagnostics.
