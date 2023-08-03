# Indo
## Judul
PEMANFAATAN AUGMENTASI DATA DALAM KLASIFIKASI HANDWRITTEN DIGIT IMAGES MENGGUNAKAN ALGORITMA CNNs BERBASIS ANDROID
## abstrak
Convolutional Neural Networks (CNN) telah menunjukkan efektivitasnya dalam handwritten digit classification dan mencapai akurasi yang bagus pada dataset MNIST. Namun seperti yang sering terjadi dalam kasus deep learning, masalah overfitting muncul ketika data pelatihan kurang mewakili sampel dari distribusi data yang akan diuji. Model yang mengalami overfitting cenderung berperforma baik pada data pelatihan tetapi buruk pada data pengujian. Teknik augmentasi data dapat digunakan untuk meningkatkan jumlah sampel dengan mengubah dan memodifikasi data asli dengan menggunakan teknik rotasi, translasi, dan zoom. Pengujian dilakukan dengan membandingkan antara model yang sebelum menggunakan data augmentasi dan model yang sudah menggunakan data augmentasi pada Aplikasi Klasifikasi Handwritten Digit pada posisi atas, bawah, kanan, kiri dan tengah. Hasil pengujian menunjukkan teknik augmentasi data efektif untuk mengatasi overfitting dan meningkatkan performa model klasifikasi handwritten digit.
## Pendahuluan

# Eng
## Title
Utilization of Data Augmentation in Handwritten Digit Image Classification Using Android-Based CNNs Algorithm
## abstract
Convolutional Neural Networks (CNN) have demonstrated their effectiveness in handwritten digit classification, achieving excellent accuracy on the MNIST dataset. However, as is often the case in deep learning, the issue of overfitting arises when the training data lacks representation of samples from the data distribution that will be tested. Overfitting models tend to perform well on the training data but poorly on the testing data. Data augmentation techniques can be employed to increase the sample size by transforming and modifying the original data using techniques such as rotation, translation, and zoom. Testing was conducted by comparing the performance of models before and after applying data augmentation in the Handwritten Digit Classification Application, considering positions such as top, bottom, right, left, and center. The results of the testing demonstrated that data augmentation techniques effectively address overfitting and improve the performance of the handwritten digit classification model.
## Introduction
Handwritten digit classification is a crucial task in image processing and computer vision, with various applications such as Postal Automation, Bank Check Processing, and Mobile Text Input. In Postal Automation, handwritten digit classification aids in address and postal code recognition. In Bank Check Processing, it helps recognize the written amount on checks. Similarly, in Mobile Text Input, it assists in text input on mobile devices.

Deep Learning algorithms like Convolutional Neural Networks (CNNs) have shown effectiveness in handwritten digit classification, achieving high accuracy on the MNIST dataset (LeCun et al., 1998). However, as with many cases in Machine Learning using Deep Learning algorithms, increasing model complexity often leads to the problem of Overfitting. Overfitting occurs when the model over-adapts to small irrelevant patterns (noise) in the training data, resulting in reduced accuracy on testing data. Overfitting models tend to perform exceptionally well on training data but poorly on testing data (Dietterich, 1995).

To address this issue, data augmentation techniques can be used to increase the data size by modifying or transforming the original data through techniques such as rotation, translation, and scaling. Based on the background mentioned above, data augmentation can be implemented to mitigate overfitting and make the model more robust against variations in input images. Additionally, the implementation will be carried out on the Android operating system using TensorFlow Lite (TFLite) as the platform. TensorFlow Lite is a framework used for executing models on mobile or Internet of Things (IoT) devices.

Therefore, the author is developing an application that can fulfill the mentioned requirements under the title "UTILIZATION OF DATA AUGMENTATION IN HANDWRITTEN DIGIT IMAGE CLASSIFICATION USING CNNS ALGORITHM ON ANDROID." Through this research, it is hoped that the performance of CNNs models in handwritten digit image classification will be enhanced, making them suitable for various handwriting recognition applications on Android-based devices and contributing to the advancement of handwriting recognition technology in the future.
## Problem Identification
1. The lack of data variation in MNIST can lead to overfitting.
2. CNNs algorithms require a large amount of training data to achieve good performance.
3. The complexity of CNNs architecture necessitates representative training data from the data distribution to be tested.
4. TFLite can only handle models of a relatively small size, so the model's size needs to be considered before converting it to an Android device.
## Scope of Problem






donwlod latex dan buat ulang.