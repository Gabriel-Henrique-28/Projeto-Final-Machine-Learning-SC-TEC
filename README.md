# Projeto-Final-Machine-Learning-SC-TEC

## Dataset utilizado: E-commerce Churn (Setor de Varejo)

## 1. Problema que o projeto resolve

Um aplicativo de vendas precisa ter a capacidade de prever quando um cliente esta prestes a abandonar o aplicativo para que seja disponibilizado um cupom de desconto para tentar reter o cliente na plataforma

Este projeto traz uma visão dos principais motivadores que faz um cliente abandonar o aplicativo, pontos importantes sobre a solução adotada para o retimento do cliente e traz uma recomendação de modelo de machine learning treinado para prever quando um cliente esta prestes abandonar o aplicativo

## 2. Resumo Executivo
### 2.1 Principais Insights da EDA

Na análise exploratória de dados, foram identificados os seguintes pontos:

- **Reclamações como principal fator de abandono**: aproximadamente metade
  dos clientes que cancelaram a assinatura haviam registrado reclamações,
  tornando esse um dos fatores mais fortes para o abandono do aplicativo identificado na análise.

- **Cupons não parecem influenciar a retenção**: o número médio de cupons
  utilizados por clientes que permaneceram na plataforma e por clientes que
  cancelaram é muito próximo.

- **Tempo de permanência como fator de retenção**: clientes que usam o aplicativo a mais tempo tendem a não abandoná-la. Além disso, esse tempo de
  permanência está significativamente correlacionado com o valor de cashback
  recebido.

**Implicação para o negócio**: esses insights sugerem que distribuir cupons
pode não ser a estratégia mais eficaz de retenção do cliente. Alternativas mais
promissoras poderiam seri o investimento em um suporte ao cliente melhor, para resolver
reclamações antes que elas levem ao cancelamento, e/ou explorar estratégias
relacionadas a cashback, dado sua correlação com o tempo de permanência.

### 2.2 Veredito do Melhor Modelo

Para escolher o melhor modelo para este negócio, deve se ter em mente algumas coisas:

Não existe um modelo perfeito, sempre haverá um trade off e neste caso o trade off é entre um modelo que ou distribuira mais cupons desnecessáriamente mas em troca distribuira mais cupons para os clientes certos, e um modelo que faz o oposto, distribui menos cupons descenessáriamente mas em troca distribuira menos cupons para os clientes certos

Para este negócio, eu julgo que é muito mais custoso um cliente abandonar a aplicativo por tempo indeterminado do que disponibilizar cupons para clientes que já ficariam na no aplicativo de qualquer jeito, pois com o lucro gerado pelos clientes retidos no aplicativo pode compensar a perda causada pelos cupons distribuidos desnecessáriamente.

Com tudo isso em mente o modelo recomendado para este negócio é o Knn, pois foi o modelo que apresentou a maior taxa de distribuição de cupons para o clientes prestes a abandonar o aplicativo e a maior taxa de distribuição de cupons desnecessários

Caso discordem da minha análise e julguem que é mais importante ter uma menor distribuição de cupons desnecessários em troca de uma menor taxa de distribuição de cupons para clientes prestes a abandonar o aplicativo, o modelo Decision Tree deve ser utilizado em produção.