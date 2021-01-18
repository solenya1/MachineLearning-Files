# Regressão Logística

O método estatístico mais utilizado para modelar *variáveis categóricas*.

*Variavel categórica: As variáveis categóricas contêm um número finito de categorias ou grupos distintos. Os dados categóricos podem não ter uma ordem lófica. Por exemplo, os preditores categóricos incluem gênero, tipo de material e método de pagamento.*


Podemos entender regressão logística como o análogo de regresão linear para problemas de classificação. Esse tipo de probela surge quando queremos **categorizar alguma variável por classes**.

Quando isso acontece, a variável **y** que queremos prever é discreta. Um exemplo seria saber se uma pessoas ganha mais de R$ 5000 anuais, com base nas suas informações socioeconômicas, ou saber se uma pessoa pedindo empréstimo vai pagar corretamente oque deverá.


Para ter uma boa visão por trás do algoritmo e oque de fato a Regressão Logística significa, deixo aqui um excelente artigo do Matheus Facure que explica detalhadamente a justifica matemática e implementação do algoritmo:


[Artigo Regressão Logística](https://matheusfacure.github.io/2017/02/25/regr-log/)


Alguns Conceitos matématicos como o Logaritmo, existem diversos materiais na internet que podem elúcidar esse conteúdo, recomendo o video do Didatica Tech sobre [O que é Logaritmo](https://www.youtube.com/watch?v=i25Knfv3PO0).


De acordo com Wikipedia a regressão logística é uma técnica estatística que tem como objetico produzir, a partide de um conjunto de observações, um modelo que permita a predição de valores tomados por uma variável categórica, frequentemente binária, a partir de uma série de variáveis explicativas contínuas e/ou binárias.


## Aplicações

A regressão logística é usada em vários campos, incluindo o aprendizado de máquina (machine learning) , a maioria dos campos médicos e ciências sociais. Por exemplo, o Trauma and Injury Severity Score (TRISS), que é amplamente utilizado para prever a mortalidade em pacientes feridos, foi originalmente desenvolvido por Boyd et al. usando regressão logística.

A regressão logística pode ser utilizada para prever o risco de desenvolver uma dada doença (por exemplo, diabetes ou doença arterial coronária), baseado em características observadas do paciente (idade, sexo, índice de massa corporal, resultados de vários testes de sangue, etc, etc.)

 Em economia ela pode ser utilizada para prever a probabilidade de uma pessoa estar trabalhando, de um proprietário optar por uma hipoteca. Campos aleatórios condicionais, uma extensão da regressão logística ao dados seqüênciais, são utilizados em processamento de linguagem natural.

## Conhecimento Importantes

Para um entendimento melhor do algoritmos se faz necessário o entendimento de alguns coneitos matemáticos importantes, entre eles estão a função Sigmóide e o conceito de logaritmo.

### Função Sigmóide

A função sigmoide ou logística e sua derivada são dadas, respectivamente, por:

![functonSig](https://sabedoriararefeita.files.wordpress.com/2016/02/ann_sigmoid.png)

A função sigmoide era a mais utilizada em RNAs, por serem biologícamente mais pausível. Como neurônios bioçógicos funcionam de forma binária (ativando vs não ativando), a função sigmoide é uma boa forma de modelar esse comportamento, já que assume valores apenas entre 0 (*nao ativação*) e 1 (*ativação*). No entanto, se olharmos sua derivada, podemos ver que ela satura para valores acima de 6 e avaixo de -5. Com essas derivadas tendendo a zero, a propagação ddo gradiente descvanece nessas regiôes, causando dificuldades no treinamento.


A função sigmoide é uma função matemática de ampo uso em campos como a economia e a computação. O nome "sigmoide" ve da for em **S** do seu gráfico como pode ser obesrvado na imagem acima.


Caso deseja aprofundar na parte da matemática da função deixo aqui um [link](https://pt.wikipedia.org/wiki/Fun%C3%A7%C3%A3o_log%C3%ADstica) para a página do Wikipédia que explica essa função e como ela funciona.


### Logaritmo

O logaritmo de um número é o expoente a que outro valor fixo, a base, deve ser elevado para produzir este número.

![logaritmo](https://static.todamateria.com.br/upload/lo/ga/logaritmodefinicao.jpg)

e para entender melhor segue um [link](https://www.youtube.com/watch?v=i25Knfv3PO0) do Didatica Tech que explica com bastante simplicidade o conceito e o gráfico gerado pelo logaritmo.


