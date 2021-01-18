## KNN (K-NEAREST-NEIGHBORS)


KNN(K — Nearest Neighbors) é um dos muitos algoritmos ( de aprendizagem supervisionada ) usado no campo de data mining e machine learning, ele é um classificador onde o aprendizado é baseado “no quão similar” é um dado (um vetor) do outro. O treinamento é formado por vetores de n dimensões.

###Como ele funciona?

O funcionamento do KNN é bem simples, imagine que você tem dados de:

* imagens de bolinhas roxas
* imagens de bolinhas amarelas
* Uma imagem de uma bolinha que você não sabe se é roxa ou amarela, mas tem todos os dados sobre ela.


Eai, como você vai fazer pra saber a cor dessa bolinha cuja a cor é desconhecida? Se ponha no lugar da máquina, imagine que você só tem os dados, você não está vendo as imagens de fato, você só está vendo o número RGB das cores de cada pixel (que são os dados que você tem da sua imagem).

obs: Vamos supor que dados com número 1 são referentes às bolinhas roxas e os dados com número 2 são referentes à bolinhas amarelas, isso apenas para facilitar a explicação, depois vamos trabalhar com dados reais.

ada linha se refere a uma imagem e cada coluna se refere a um pixel dessa imagem, na última coluna nós temos a classe (cor) de cada uma das bolinhas, R ->roxo, e A -> amarelo, temos lá 5 imagens (5 linhas) de bolinhas, cada uma com sua classificação, você pode tentar descobrir a cor (no caso a classe) da nova imagem (uma imagem de uma bolinha que você não sabe a cor) de N maneiras, uma dessas N maneiras é ficar comparando essa nova imagem com todas as outras, e ver com qual ela se parece mais, se os dados dessa nova imagem (que você não sabe a classe dela) são mais próximos dos dados das imagens de bolinhas amarelas, então a cor da imagem nova que não está classificado é amarela, se os dados da imagem nova, forem mais parecidos com os dados das imagens de bolinha roxa, então essa a cor da bolinha da imagem nova é roxa, parece bobo mas é quase isso que o knn faz, só que de uma forma mais sofisticada.

No caso do KNN, ele não “compara” o seu novo dado (não classificado) com todos os outros de fato, na verdade ele executa um cálculo matemático para medir a distância entre os dados para fazer sua classificação, (que é quaaaaaaaaaaaase a mesma coisa #soqnao). Esse cálculo que estou falando pode ser qualquer um que meça a distância entre dois pontos, como por exemplo: Euclidiana, Manhattan, Minkowski, Ponderada e etc.

As etapas de um algoritmo KNN são:

1. Recebe um dado não classificado;
2. Mede a distância (Euclidiana, Manhattan, Minkowski ou Ponderada) do novo; dado com todos os outros dados que já estão classificados;
3. Obtém as X(no caso essa variável X é o parâmetro K) menores distâncias;
4. Verifica a classe de cada da um dos dados que tiveram a menor distância e conta a quantidade de cada classe que aparece;
5. Toma como resultado a classe que mais apareceu dentre os dados que tiveram as menores distâncias;
6. Classifica o novo dado com a classe tomada como resultado da classificação.



