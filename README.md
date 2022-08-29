# Train_DNN

Train DNN digunakan untuk tackle sebuah complex problem pada sebuah ANN arsitektur (mendteksi ratusan sebuah gambar di dalam high resolution image), 
pada implementasi trainng ANN menggunakan backprogation methode :
- forward methode (calculation result) 
- backward methode (calculation gradient loss function on weight with chain rule)
terjadi beberapa masalah :

- vanashing dan exploding gradient => sering muncul pada penggunaan sigmod / logistic acitvy function pada pemberian data yang rendah atau komplex
sehingga lower layer to be hard to train dan pada backward tidak terjadi perubahan pada kalkulasi sebuah loss function di setiap weight conection sehingga 
model train never get good solution  
- not enough train data untuk large network atau sangat mahal pada pemberian label
- proses train sangat lama karena banyak nya proses kalkulasi pada beratnya network di hyperparameter yang diberikan
- transfer learning and unspervised pretrained
- various optimizers
- regulation models

- Vanashing gradient dapat dihindari dengan melakukan
  - weight random initializer glorot, he, lecuan
  - batch normalization agar scale setiap output layer pada neural network tidak kembali mengalami vanashing ada exploding
  - fast optimizer : momentum, Nestrov accrelation gradient(NAG),Ada grad,rmsprop adam,adammax,nadam
  - learning_rate scheduling : power, exponensial,piecwise cosntant scheduling,performance scheduling,1cycle scheduling
