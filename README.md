# Trabalho Final de Graduação (TFG)

Repositório criado para armezar o código e a monografia desenvolvidos durante o meu trabalho final de graduação do curso de Ciência da Computação na Universidade Federal de Itajubá (UNIFEI).

README ainda em desenvolvimento!

## Tema

Comparação de algoritmos de aprendizado profundo na classificação de comentários contendo discurso de ódio na internet.

## Metodologia

O conjunto de dados foi extraído do site Analytics Vidhya e é composto por dois arquivos: de treinamento, para treinar o modelo, e o de teste, para avaliar o modelo dentro da competição oficial hospedada no site.

Também foi realizado experimentos com e sem balanceamento dos dados (utilizando a técnica de sobreamostragem) e com pré-processamento a fim de verificar se ocorre alguma melhoria nos modelos desenvolvidos.

Os algoritmos de aprendizado profundo utilizados foram: Rede Neural Convolucional (RNC) e Long Short-Term Memory (LSTM).

Foram utilizadas duas sementes (seeds) para que os resultados possam ser reproduzidos novamente e fielmente comparados entre si (sem se preocupar com a inicialização aleatória das variáveis dos modelos): 23 e 2109.

## Resultados

A utilização da técnica de balanceamento dos dados gerou melhorias nos modelos testados, ao contrário do pré-processamento. O melhor modelo, tanto em tempo de execução quanto na avaliação nos dados de validação e de teste, foi a LSTM.

## Bibliotecas utilizadas

* RE;
* Scikit-Learn;
* Keras;
* Pandas;
* Numpy;
* NLTK;
* Imblearn;
* Matplotlib e Seaborn;

## Autor

<a href="linkedin.com/in/rafaelgreca">Rafael Greca Vieira</a>