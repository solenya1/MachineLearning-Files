# Validação Cruzada

validação cruzada é uma técnica para avaliar modelos de ML por meio de treinamento de vário modelos de ML em subconjuntos de dados de entrada disponíveis e avaliação deles no subconjunto complementar dos dados. Use a validação cruzada para detectar sobreajuste, ou seja, a não generalização de um padrão.


## Validação Cruzada K-fold

Na validação cruzada k-fold, você divide os dados de entrada em subconjuntos de dados k *(também chamados de folds)*. Você treina um modelo de ML em todos os subconjuntos, exceto um (k-1) e depois avalia o modelo no subconjunto que não foi usado para o treinamento. Esse processo é repetido k vezes, com um subconjunto diferente reservado para avaliação *(e excluído do treinamento)* a cada vez.


O diagrama a seguir mostra um exemplo de subconjunto de treinamento e subconjuntos de avaliação complementar gerados para cada um dos quatro modelo que são criados e treinados durante uma validação cruzada 4-fold. O modelo um usa os primeiro 25% dos dados para avaliação e os 75% restante para treinamento. O modelo dois usa o segundo subconjunto de 25 por cento *(25 a 50 por cento)* para avaliação, e os três subconjuntos restantes de dados para treinamento e assim por diante.

![exemplo](https://amzn.to/2ZHKsqj)

Cada modelo é treinado e avaliado usando fontes de dados complementares. Os dados na fonte de dados de avaliação incluem e são limitados a todos os dados que não aparecem na fonte de dados de treinamento. 

Exemplo do esquema de particionamento e execução do método k-fold com `k=3`.

![wikimage](https://bit.ly/3c2fWfZ)
