## Modelos

### TextCNN 1D

Versão original:

* Embedding dim = 300
* Filters = 100
* Kernel size = [3, 4, 5]
* Dropout rate = 0.5
* l2 constraint = 3
* Epochs = 10
* Batch size = 100
* Length size = 30
* Non linearity function = 'relu'
* Activation function = 'sigmoid'
* Conv1D padding = 'valid'
* 1 hidden layer = Concatenação de 3 camadas CNN1D com os filtros e tamanhos de kernel citados

Versão original padding adaptado:

* Embedding dim = 300
* Filters = 100
* Kernel size = [3, 4, 5]
* Dropout rate = 0.5
* l2 constraint = 3
* Epochs = 10
* Batch size = 100
* Length size = 30
* Non linearity function = 'relu'
* Activation function = 'sigmoid'
* Conv1D padding = 'same'
* 1 hidden layer = Concatenação de 3 camadas CNN1D com os filtros e tamanhos de kernel citados

### TextCNN 2D

Versão original padding adaptado:

* Embedding dim = 300
* Filters = 100
* Kernel size = [(3, 300), (4, 300), (5, 300)]
* Dropout rate = 0.5
* l2 constraint = 3
* Epochs = 10
* Batch size = 100
* Length size = 30
* Input = (30, 300)
* Non linearity function = 'relu'
* Activation function = 'sigmoid'
* Conv2D padding = 'valid'
* MaxPooling2D padding = 'valid'
* MaxPooling2D pool_size = [(30 - 3 + 1, 1), (30 - 4 + 1, 1), (30 - 5 + 1, 1)]
* 1 hidden layer = Concatenação de 3 camadas CNN2D com os filtros e tamanhos de kernel citados

## Resultados Modelos
