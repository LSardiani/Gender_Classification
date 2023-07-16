# Gender Classification using CelebA Dataset

Hello there!
This project was the first project (Project 1) from IndonesiaAI Computer Vision (CV) Bootcamp Batch 2.

We extracted the dataset CelebA Dataset (https://www.kaggle.com/datasets/jessicali9530/celeba-dataset) and only using 5000 images.

# Background
Face recognition plays an important role in our daily activity tasks; itcan be very useful for security and access control applications. 

The way humans perceive gender relies not only on the face region perception but also on the surroundings, such as skin tone, hair, and wearing attributes such as hats, eyeglasses, earrings, etc. 

Gender classification based on facial images has received increased attention in the community of Computer Vision, and there were several models which showed better performance, for example, VGG19 and InceptionV3. 

# Getting started
The dataset was downloaded from https://drive.google.com/drive/folders/19MRsL8ZWR9mXme-bSodyAUHrwIT2Eig7?usp=drive_link

After unzipped it, use the file 'image_attributes_filtered.csv' [image_attributes_filtered.csv](https://github.com/LSardiani/Gender_Classification/files/12063725/image_attributes_filtered.csv)

Please do not forget to replace -1 with 0 (female code) in the data, and balancing the male and female data.

# Model

Transfer learning: VGG-19

Train : test : validation = 70 : 20 : 10 


Using Data augmentation

Unfreeze -5 layers Fully Connected Layer, Flatten

HL-1 Dense(512), relu, Dropout(0.2)

HL-2 Dense(256), relu, Dropout(0.2)

HL-3 Dense(64), relu, Dropout(0.2)

HL-4 Dense(32), relu, Dropout(0.2)

OL   Dense(2), softmax

Batch size: 32; Learning rate: 0.0001; Epoch: 10; Loss function: SparseCategoricalCrossentropy

Training time: 0.07 hours

# Results

Training and Validation Curves

![Validation_Curves_Experiment_2](https://github.com/LSardiani/Gender_Classification/assets/135226112/28f03ccc-c970-4205-aa2a-9d5225a2ca9a)

# Confusion Matrix
![Confusion_Experiment_2](https://github.com/LSardiani/Gender_Classification/assets/135226112/e2cef604-d252-455d-a160-f15c588279dd)

              precision    recall  f1-score   support

        Male       0.98      0.91      0.95       396
      Female       0.93      0.98      0.95       427

    accuracy                           0.95       823
    macro avg      0.95      0.95      0.95       823
    weighted avg   0.96      0.95      0.95       823

# Actual prediction
![Foto_Aktual_vs_Prediksi_VGG_Experiment](https://github.com/LSardiani/Gender_Classification/assets/135226112/a837525b-d23d-4cc7-a28e-8467936b1844)

# Wrong prediction Female
![Female_di_Prediksi_sebagai_Male_VGG_Experiment](https://github.com/LSardiani/Gender_Classification/assets/135226112/c7ed19c1-f4fb-4bb4-9f26-01ed8cc19a3c)

# Wrong prediction Male
![Male_di_Prediksi_sebagai_Female_VGG_Experiment](https://github.com/LSardiani/Gender_Classification/assets/135226112/f8220b35-d791-428e-a93a-0f5df15f8ab9)

# Contact
Please reach me on my email: lilysilva.dr@gmail.com for any further discussion.
Thank you!
