## Modelos

### Modelo1

* Embedding dim = 300
* Length size = 30
* Conv1D = 32 filters, kernel size 3, padding 'same'
* Dropout rate = 0.2
* Activation function = 'sigmoid'
* Non linearity function = 'relu'

Embedding -> Conv1D -> MaxPooling1D -> Flatten -> Dropout -> Dense

### Modelo2

* Embedding dim = 300
* Length size = 30
* Conv1D = 32 filters, kernel size 3, padding 'same'
* Conv1D = 64 filters, kernel size 5, padding 'same'
* Dropout rate = 0.2
* Activation function = 'sigmoid'
* Non linearity function = 'relu'

Embedding -> Conv1D -> MaxPooling1D -> Conv1D -> MaxPooling1D -> Flatten -> Dropout -> Dense

### Modelo3

* Embedding dim = 300
* Length size = 30
* Conv1D = 32 filters, kernel size 3, padding 'same'
* Conv1D = 64 filters, kernel size 5, padding 'same'
* Conv1D = 128 filters, kernel size 7, padding 'same'
* Dropout rate = 0.2
* Activation function = 'sigmoid'
* Non linearity function = 'relu'

Embedding -> Conv1D -> MaxPooling1D -> Conv1D -> MaxPooling1D -> Conv1D -> MaxPooling1D -> Flatten -> Dropout -> Dense

### Modelo4

* Embedding dim = 300
* Length size = 30
* Conv1D = 32 filters, kernel size 3, padding 'same'
* Conv1D = 64 filters, kernel size 5, padding 'same'
* Dropout rate = 0.2
* Activation function = 'sigmoid'
* Non linearity function = 'relu'
* Dense = 64 units

Embedding -> Conv1D -> MaxPooling1D -> Conv1D -> MaxPooling1D -> Flatten -> Dropout -> Dense -> Dense

### Modelo5

* Embedding dim = 300
* Length size = 30
* Conv1D = 32 filters, kernel size 3, padding 'same'
* Dropout rate = 0.2
* Activation function = 'sigmoid'
* Non linearity function = 'relu'
* Dense = 64 units

Embedding -> Conv1D -> MaxPooling1D -> Flatten -> Dropout -> Dense -> Dense

### Modelo6

* Embedding dim = 300
* Length size = 30
* Conv1D = 32 filters, kernel size 3, padding 'same'
* Conv1D = 64 filters, kernel size 5, padding 'same'
* Conv1D = 128 filters, kernel size 7, padding 'same'
* Dropout rate = 0.2
* Activation function = 'sigmoid'
* Non linearity function = 'relu'
* Dense = 64 units

Embedding -> Conv1D -> MaxPooling1D -> Conv1D -> MaxPooling1D -> Conv1D -> MaxPooling1D -> Flatten -> Dropout -> Dense -> Dense

## Resultados Modelos

Model | Preprocessing | Augmentation | F1 Score
--- | --- | --- | ---
modelo1 | False | False | 0.69448
modelo1 | False | True | 0.72085
modelo1 | True | False | 0.69677
**modelo1** | **True** | **True** | **0.74107**
modelo2 | False | False | 0.70326
modelo2 | False | True | 0.71794
modelo2 | True | False | 0.71826
modelo2 | True | True | 0.70245
modelo3 | False | False | 0.70440
modelo3 | False | True | 0.73701
modelo3 | True | False | 0.7
modelo3 | True | True | 0.69440
modelo4 | False | False | 0.70759
modelo4 | False | True | 0.69551
modelo4 | True | False | 0.71320
modelo4 | True | True | 0.71542
modelo5 | False | False | 0.69553
modelo5 | False | True | 0.71090
modelo5 | True | False | 0.68759
modelo5 | True | True | 0.70087
modelo6 | False | False | 0.69579
modelo6 | False | True | 0.72455
modelo6 | True | False | 0.70820
modelo6 | True | True | 0.67482