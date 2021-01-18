# Curva ROC

uma cruva ROC (*receiver operating characteristic curve*) é um grafico que mostra a perfomance do modelo de classificação dentro dos limites de classificação. Essa curva mostra dois parâmetros

* Taxa de Positivos Verdadeiros (*True Positive - TP*)
* Taxa de falso Positivo (*False Positive - FP*)


A formula da Taxa de Verdadeiros Positivos é definida como sendo :

`TPR = (TP) / (TP + FN)`

Os True Positive dividido pela soma dos True Positive e False Negative. E a formula da taxa dos Falso Positive é definida da seguinte forma:

`FPR = (FP) / (FP + TN)`

Ou seja A taxa de Falso positivo é a divisão dos Falso positivos pela soma dos falso positivos pelos Verdadeiros Negativos.

Uma curva ROC plota TPR vs. FPR em diferentes limiares de classificação. Baixar o limiar de classificação classifica mais itens como positivos, aumentando assim tanto os Positivos Falsos como os Positivos Verdadeiros. A figura a seguir mostra uma curva ROC típica.

![image1](https://i.ibb.co/FKqbpNS/ROCCurve.png)

# AUC : Area Under the ROC Curve

AUC siginifica "*Area under the ROC Curve*"( Àrea abaixo da curva ROC). AUC mede toda a bi-dimensional area abaixo da curva ROC (*Pense em cálculo de integral*) de (0, 0) a (1, 1).

![image2](https://i.ibb.co/tLgThfg/AUC.png)

AUC representa a probabilidade de que um exemplo aleatório positivo (verde) seja posicionado à direita de um exemplo aleatório negativo (vermelho).

O AUC varia em valor de 0 a 1. Um modelo cujas previsões estão 100% erradas tem um AUC de 0,0; um modelo cujas previsões estão 100% corretas tem um AUC de 1,0.

O AUC é desejável pelas duas razões a seguir:

O AUC é variável em escala. Ela mede o quão bem as previsões são classificadas, ao invés de seus valores absolutos.
AUC é classifica-invariante. Ela mede a qualidade das previsões do modelo, independentemente do limiar de classificação escolhido.
Entretanto, ambas as razões vêm com advertências, o que pode limitar a utilidade da AUC em certos casos de uso:

A invariância da escala nem sempre é desejável. Por exemplo, às vezes realmente precisamos de resultados de probabilidade bem calibrados, e a AUC não nos informa sobre isso.

A invariância da escala nem sempre é desejável. Em casos onde há grandes disparidades no custo de falsos negativos versus falsos positivos, pode ser crítico minimizar um tipo de erro de classificação. Por exemplo, ao fazer a detecção de spam por e-mail, é provável que você queira priorizar a minimização de falsos positivos (mesmo que isso resulte em um aumento significativo de falsos negativos). A AUC não é uma métrica útil para este tipo de otimização.

