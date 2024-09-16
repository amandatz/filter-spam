# Naive Bayes Spam Filter

Este projeto, proposto na disciplina de **Aprendizado de Máquina**, tem como objetivo classificar e-mails como spam ou legítimos utilizando o algoritmo _Naive Bayes_.

O trabalho precisa conter:
1. [Implementar os tópicos em "ToDo";](#implementar-todos)
2. [Explicar o que significa "Bag of Words";](#bag-of-words)
2. [Explicar a diferença entre especificidade e sensitividade;](#especificidade-x-sensitividade)
2. [Implementar o Naive Bayes e comparar com um dos algoritmos vistos no ML tour;](#naive-bayes-x-regressão-logística)
2. [Fazer uma lista dos prós e contras do Naive Bayes e do algoritmo escolhido.](#prós-e-contras)

## Implementar ToDos

> **Instrução:** Responder/implementar corretamente todos os tópicos em "ToDo"

Este tópico foi inteiramente resolvido dentro de [Bayesian_Inference.ipynb](Bayesian_Inference.ipynb)

## Bag of Words

> **Instrução:** Explicar o que significa o "Bag of Words"

_Bag of Words_ (BoW) é uma técnica utilizada para representar dados de texto como um vetor numérico. Ela essencialmente conta a frequência de palavras ignorando a ordem em que elas ocorrem.

De forma exemplificada, considere as seguintes frases:
- **Frase 0:** O tempo perguntou ao tempo quanto tempo o tempo tem
- **Frase 1:** Uma breve história do tempo

Podemos visualizá-las em forma de matriz: cada linha `i` representa uma frase, enquanto a coluna `j` representa uma palavra. A entrada `ij` da matriz guarda a frequência em que a palavra `j` aparece na frase `i`. 

Ignorando a diferença entre maiúsculas e minúsculas, teríamos:

|   | o | tempo | perguntou | ao | quanto | tem | uma | breve | história | do |
|:-:|:-:|:-----:|:---------:|:--:|:------:|:---:|:---:|:-----:|:--------:|:--:|
| **0** | 2 | 4 | 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 |
| **1** | 0 | 1 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 |

## Especificidade x Sensitividade

> **Instrução:** Explicar a diferença entre especificidade e sensitividade. Dê dois exemplos práticos, uma em que a especificidade parece ser mais adequada do que a sensitividade e vice-versa

A **sensitividade** de um teste, também chamada de taxa de verdadeiro positivo (TPR) ou  _recall_, é a taxa de positivos que foram corretamente identificados como positivos

A sensibilidade pode ser calculada da seguinte forma:
```
sensibilidade = #[verdadeiros positivos] / (#[verdadeiros positivos] + #[falsos negativos])
```

Já a **especificidade** de um teste, também chamada de taxa de verdadeiro negativo (TNR), é a taxa de negativos que foram corretamente identificados como negativos, i.e, 
```
especificidade = #[verdadeiros negativos] / (#[verdadeiros negativos] + #[falsos positivos])
```

A escolha entre algoritmos que priorizam sensibilidade ou especificidade depende diretamente da natureza do problema.

Por exemplo, em um teste para detecção de câncer, é importante priorizar a sensitividade para garantir que a maior parte dos casos positivos seja identificada. Perder um positivo (paciente com câncer) por falta de tratamento seria muito grave.

Em contrapartida, um filtro de spam deve priorizar a especificidade. Visualizar um spam é menos pior do que perder uma mensagem importante.

## Naive Bayes x Regressão logística

> **Instrução:** Implementar o Naive Bayes conforme indica o roteiro e comparar com um (1) dos algoritmos vistos no ML tour, justificando a escolha do melhor modelo. É para comparar o Naive Bayes com um e apenas um algoritmo

## Prós e contras

> **Instrução:** Você deverá fazer uma lista dos prós e contras do Naive Bayes e do algoritmo escolhido. Você deve explicar o resultado obtido com base nas características dos dois algoritmos avaliado. Você teria algum insight relevante para me apresentar?

