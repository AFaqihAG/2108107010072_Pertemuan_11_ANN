Tugas ini berfokus pada Artificial Neural Networks (ANN) dan perbandingannya terhadap SVM.

Dataset saya ambil pada kaggle.

**Iris Flower, SVM Classification** : https://www.kaggle.com/datasets/uciml/iris?resource=download

Dataset berisikan data jenis-jenis Iris Flower.

Di bawah ini merupakan kolom-kolom pada dataset:
* Id
* SepalLengthCm : Panjang sepal bunga dalam centimeter
* SepalWidthCm  : Lebar sepal bunga dalam centimeter
* PetalLengthCm : Panjang petal bunga dalam centimeter
* PetalWidthCm  : Lebar petal bunga dalam centimeter
* Species       : Jenis species bunga

Menggunakan ANN, saya membuat sebuah model untuk memprediksi label "Species" berdasarkan nilai dari atribut-atributnya.

Berikut rangkuman hasil model ANN dan perbandingannya :

## ANN

    ...
    11/11 ━━━━━━━━━━━━━━━━━━━━ 0s 3ms/step - accuracy: 0.9810 - loss: 0.0778 - val_accuracy: 0.9778 - val_loss: 0.1116
    Epoch 200/200
    11/11 ━━━━━━━━━━━━━━━━━━━━ 0s 2ms/step - accuracy: 0.9682 - loss: 0.1059 - val_accuracy: 0.9778 - val_loss: 0.1076
    2/2 ━━━━━━━━━━━━━━━━━━━━ 0s 21ms/step

Pada iterasi terakhir, diperoleh nilai akurasi training sebesar 0.9682 dan akurasi testing 0.9778.

## SVM

Pada svm saya membuat dua model, Model pertama menggunakan kolom SepalLength dan PetalLength, model kedua menggunakan SepalWidth dan PetalWidth.

### Model Pertama

    Model Classification Report Result
                  precision    recall  f1-score   support
    
               0       1.00      1.00      1.00        13
               1       1.00      0.94      0.97        16
               2       0.90      1.00      0.95         9
    
        accuracy                           0.97        38
       macro avg       0.97      0.98      0.97        38
    weighted avg       0.98      0.97      0.97        38
    
Menggunakan kolom SepalLength dan PetalLength, diperoleh nilai akurasi 97%

### Model Kedua

    Model Classification Report Result
                  precision    recall  f1-score   support
    
               0       1.00      1.00      1.00        13
               1       0.94      0.94      0.94        16
               2       0.89      0.89      0.89         9
    
        accuracy                           0.95        38
       macro avg       0.94      0.94      0.94        38
    weighted avg       0.95      0.95      0.95        38
    
Menggunakan kolom SepalWidth dan PetalWidth, diperoleh nilai akurasi 95%

