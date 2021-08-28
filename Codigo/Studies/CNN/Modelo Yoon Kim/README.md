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

### TextCNN1D

Arquitetura | Model | Preprocessing | Augmentation | F1 Score
--- | --- | --- | --- | ---
original | rand | False | False | 0
original | rand | True | False | 0
**original** | **rand** | **False** | **True** | **0.73452**
original | rand | True | True | 0.70514
original | non_static | False | False | 0
original | non_static | True | False | 0
original | non_static | False | True | 0.67894
original | non_static | True | True | 0.66666
modificado | rand | False | False | 0.64714
modificado | rand | True | False | 0.62857
modificado | rand | False | True | 0.67447
modificado | rand | True | True | 0.69146
modificado | non_static | False | False | 0.67942
modificado | non_static | True | False | 0.59926
**modificado** | **non_static** | **False** | **True** | **0.71601**
modificado | non_static | True | True | 0.69170

### TextCNN2D

Arquitetura | Model | Preprocessing | Augmentation | F1 Score
--- | --- | --- | --- | ---
original | rand | False | False | 0.44508
original | rand | True | False | 0.41185
original | rand | False | True | 0.68578
original | rand | True | True | 0.73655
original | non_static | False | False | 0.31027
original | non_static | True | False | 0.40344
original | non_static | False | True | 0.73668
**original** | **non_static** | **True** | **True** | **0.74261**
modificado | rand | False | False | 0.65610
modificado | rand | True | False | 0.61355
**modificado** | **rand** | **False** | **True** | **0.71727**
modificado | rand | True | True | 0.69620
modificado | non_static | False | False | 0.64297
modificado | non_static | True | False | 0.65798
modificado | non_static | False | True | 0.67025
modificado | non_static | True | True | 0.70914