# Mentoria Awari

## Objetivo

Entender o caminho para atuar como engenheiro de machine learning

## Método

O mentor irá orientar um caso real mostrando todas as boas práticas, ferramentas e habilidades para executar como um Engenheiro de Machine Learning na vida real

## Caso

### Introdução

Atualmente estou trabalhando em paralelo com meu trabalho atual, desenvolvendo 2 soluções que podem envolver machine learning:

*  Um algoritmo de forecasting de insumos de restaurante, que tem o objetivo de indicar aumento ou diminuição de preços os insumos conforme a sazonalidade.
*  Uma função de otimização que sugeri preços que podem aumentar as vendas (aqui foi utilizado machine learning, foi utilizado técnicas de otimização clássica da matemática, estou passando em usar Reinforcement learning como o Multi-armed Bandits (o que é mais interessante para o nosso projeto)

### Projeto

O objetivo é construir um sistema inteligente de micro serviços que posam ser consumidos via API, de forma que seja fácil integração com qualquer APP.

#### Dados e modelagem

Os dados são basicamente o histórico de vendas e compras de pratos e insumos dos restaurantes, conforme novos clientes forem adquiridos, o histórico de vendas será adicionado na base gerando uma tabela longa, o objetivo é ter apenas um modelo ao invés de um para cada cliente ou item que será treinado por uma única fonte de dados, a discriminação dos restaurantes inicialmente será diferenciada pelo ID, mas futuramente deverá ter outras features que possa caracterizar mais para o modelo.

#### Confidencialidade dos dados (Há discutir)

Como os dados são reais, não é ético trabalhamos com eles, então, vou procurar por dados livres que correspondam o mais próximo possível da realidade do projeto original, outro ponto, é que atualmente há poucos dados, então o processo de modelagem não está confiável por falta de dados, usar uma base maior poder ser um benefício para além de poder compartilhar para comunidade.

#### Arquitetura

Será discuto com o mentor, mas atualmente está da seguinte forma:

2 API's:

* Treinamento
  *  Dispara um código de treinamento passando o ID do restaurante
  * Treina um modelo para cada item e para cada restaurante
* Forecating
  * Sugestão de preco passando o ID do restaurante e ID do item
  * Forecating do preco dos insumos para saber se vai aumentar ou nao passando o ID do restaurante e ID do item

As apis entao implementadas em docker que estão subindo como microservicos no back-end do APP.
