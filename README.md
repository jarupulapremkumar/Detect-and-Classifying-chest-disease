# Detect-and-Classifying-chest-disease
### Summary:
  - AI/ML/DL has been revolutionizing healthcare and medicine:
    - Medical imagery 
    - Drug research 
    - Genome development 
  - Deep learning has been proven to be superior in detecting and classifying disease using imagery data.
  - Skin cancer could be detected more accurately by Deep Learning than by dermatologists (2018). 
    - Human dermatologists detection = 86.6%
    - Deep Learning detection = 95%
    
### Outcome:
  - In this case study, we will assume that you work as a Deep Learning Consultant. 
  - You have been hired by a hospital in downtown Toronto and you have been tasked to automate the process of detecting and classifying chest disease and reduce the cost and time of detection. 
  - The team has collected extensive X-Ray chest data and they approached you to develop a model that could detect and classify the diseases in less than 1 minute.
  
### About Data :
  - You have been provided with 133 images that belong to 4 classes: 
    - Healthy 
    - Covid-19
    - Bacterial Pneumonia
    - Viral Pneumonia 
### Models :
  **CNN:**
    - The first CNN layers are used to extract high level general features. 
    - The last couple of layers are used to perform classification (on a specific task).
    - Local respective fields scan the image first searching for simple shapes such as edges/lines 
    - These edges are then picked up by the subsequent layer to form more complex features.![image](https://user-images.githubusercontent.com/46964929/180596265-36a2f38c-b14f-43b0-8f87-f80c6871a0bd.png)
    
  **ResNet (Transfer Learning):**
    - As CNNs grow deeper, vanishing gradient tend to occur which negatively impact network performance.
    - Vanishing gradient problem occurs when the gradient is back-propagated to earlier layers which results in a very small gradient. 
    - Residual Neural Network includes “skip connection” feature which enables training of 152 layers without vanishing gradient issues. 
    - Resnet works by adding “identity mappings” on top of the CNN. 
    - ImageNet contains 11 million images and 11,000 categories. 
    - ImageNet is used to train ResNet deep network.![image](https://user-images.githubusercontent.com/46964929/180596600-ce5dc654-1649-481f-bc53-c17cb826659c.png)

    
  **TRANSFER LEARNING TRAINING STRATEGIES:**
    - Strategy #1 Steps: 
      - Freeze the trained CNN network weights from the first layers. 
      - Only train the newly added dense layers (with randomly initialized weights).
    - Strategy #2 Steps: 
      - Initialize the CNN network with the pre-trained weights 
      - Retrain the entire CNN network while setting the learning rate to be very small, 
      this is critical to ensure that you do not aggressively change the trained weights.
    - Transfer learning advantages are:
      - Provides fast training progress, you don’t have to start from scratch using randomly initialized weights
      - You can use small training dataset to achieve incredible results![image](https://user-images.githubusercontent.com/46964929/180596357-3c6551ed-f72c-433f-a1cb-cab3994a679d.png)
    














