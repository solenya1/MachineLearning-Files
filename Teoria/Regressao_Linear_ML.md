# Regressão Linear (Conceito + Matemática)

## Gradiente Descendente

Gradiente descendente é um do algoritmos de maior sucesso em problemas de Machine Learning. O método consiste em encontrar, de forma iterativa, os valores dos parâmetros que minimizam determinada função de interesse.

Video Explicando:

 <iframe width="560" height="315" src="https://www.youtube.com/embed/htfh2xrnlaE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Coeficiente de determinação R2

O coeficiente de determinação, também chamado de R2, é uma medida de ajuste de um modelo estátistico linear generalizado, como a regressão linear simples ou múltipla, aos valores observados de uma variável aleatória. O R2 varia entre 0 e 1, por vezes sendo expresso em termos percentuais. Nesse caso, expressa a quantidade e variância dos dados que é explicada pelo modelo linear. Assim, quanto maior o R2, mais explicativo é o modelo linear, ou seja, melhor ele se ajusta à amostra.

Video Explicando:

<iframe width="560" height="315" src="https://www.youtube.com/embed/wDJjmH3JFqc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Ridge Regression

A Ridge Regression é um método de regularização do modelo que tem como principal objetivo suvizxar atributos que sejam relacionados uns aos outros e que aumentam o ruído do modelo (A.K.A multicolinearidade). Com isso com a retirada de determinados atributos do modelo, o mesmo converge para um resultado muito maius estável em que com a redução desses atributos, a redução em termos de acuácia do modelo se mantêm inalterada; O mecanismo algoritmico que faz isso é atravéz de um mecanismo de penalização que coloca um viés e que vai reduzindo os valores os betas até não zero.

Com isso os atributos que contribuem menos para o poder preditivo do modelo são levados para a irrelevância usando esse mecanismo de penalização do viés.


## Regularização L1, L2 e Regressão Lasso

Como já sabemos uma regressão linear tenta ajustar uma função linear ao dados:

![formula](https://miro.medium.com/max/316/1*Ta_6UL6CaGZU7pvL7BMsLQ.png)

O precedimento de ajuste envolve a função de custo como soma residual dos quadrados ou RSS. Os coeficientes *w* são escolhidos para minimizar essa função de custo com base nos dados de treinamento:

![formula2](https://miro.medium.com/max/327/1*UFsN2JHfP5t_E1a9icTbwQ.png)

No entanto pode ocorrer overfitting, ou seja, o modelo pode *"decorar"* o ruído dos dados de treinamento. Nesse caso, dizemos que o modelo tem um erro de generalização elevado.

Para isso, regularizamos os coeficiente *w*, ou seja, restringimos o seu tamanho. Isso é feito adicionando um termo na função como no caso do **Ridge Regression** 

### Lasso (ou L1)

![FORMULA3](https://miro.medium.com/max/535/1*dynW6DLJxX2iaMrnfgxk_A.png)

Além de diminuit a variância do modelo, essa regularização tem outra importante aplicação em ML. A regularização Lasso seleciona apenas uma dessas features e zera os coeficientes das outras, de forma a minimar a penalização L1.
Isso facilita a interpretação do modelo, oque é uma vantagem.

### Elatic Net -- L1 + L2

Se trata de combinar os termos de regularização **Lasso** e **Ridge**. Assim, obtemos o melhor dos dois mundo, porém temos que enfrentar o problema de determinar dois hiperparâmetros para obter soluções ótimas.

![formula4](https://miro.medium.com/max/693/1*elv_EM7V-1QvnVkD0Mmk8Q.png)

### Comparação entre os métodos de regularização

![graficos](https://miro.medium.com/max/3161/1*PdC1TQDuQUepWpVLgswTmQ.png)

Podemos observar que a regressão com regularização Lasso tende a ignorar relações fracas, emquanto a regressão com regularização Ridge considera também relações fracas, mas não lida tão bem com relações fortes. A regressão Elastic Net é um intermediário entre **Ridge** e **Lasso**
