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
* MaxPooling1D pool_size = [30 - 3 + 1, 30 - 4 + 1, 30 - 5 + 1]
* 1 hidden layer = Concatenação de 3 camadas CNN1D com os filtros e tamanhos de kernel citados

Versão modificada:

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
* MaxPooling1D pool_size = [2, 2, 2]
* 1 hidden layer = Concatenação de 3 camadas CNN1D com os filtros e tamanhos de kernel citados

### TextCNN 2D

Versão original:

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

Versão modificada:

Versão original:

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
* MaxPooling2D pool_size = [(2, 1), (2, 1), (2, 1)]
* 1 hidden layer = Concatenação de 3 camadas CNN2D com os filtros e tamanhos de kernel citados

## Resultados Modelos

As arquiteturas originais foram desconsideradas por motivos de performance.

### TextCNN1D

Arquitetura | Model | Preprocessing | Augmentation | F1 Score
--- | --- | --- | --- | ---
modificado | rand | False | False | 0.65573
modificado | rand | True | False | 0.58691
modificado | rand | False | True | 0.70122
**modificado** | **rand** | **True** | **True** | **0.70308**
modificado | non_static | False | False | 0.66993
modificado | non_static | True | False | 0.62118
modificado | non_static | False | True | 0.6838
modificado | non_static | True | True | 0.69958

### TextCNN2D

Arquitetura | Model | Preprocessing | Augmentation | F1 Score
--- | --- | --- | --- | ---
modificado | rand | False | False | 0.64401
modificado | rand | True | False | 0.54510
modificado | rand | False | True | 0.70463
**modificado** | **rand** | **True** | **True** | **0.72103**
modificado | non_static | False | False | 0.65279
modificado | non_static | True | False | 0.53021
modificado | non_static | False | True | 0.69019
modificado | non_static | True | True | 0.69824