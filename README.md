# Análise e Tratamento de Dados do Clima

Este projeto foca na análise exploratória e no tratamento de um conjunto de dados sobre as condições climáticas e a decisão de jogar, visando preparar os dados para futuras análises ou modelos preditivos.

## Situação a ser Analisada
O objetivo principal deste projeto é identificar e corrigir inconsistências e valores anômalos em um dataset de condições climáticas (`tempo.csv`). As colunas 'Aparencia', 'Temperatura', 'Umidade' e 'Vento' foram analisadas individualmente para garantir a integridade dos dados.

## Base
O conjunto de dados utilizado foi `tempo.csv`.

## Dados
O dataset contém as seguintes colunas:
- `Aparencia`: Condição do céu (sol, nublado, chuva).
- `Temperatura`: Temperatura ambiente.
- `Umidade`: Nível de umidade.
- `Vento`: Presença de vento (VERDADEIRO/FALSO).
- `Jogar`: Decisão de jogar (sim/nao).

Inicialmente, foi verificado que o dataset não possuía valores nulos óbvios, mas uma análise mais aprofundada revelou a presença de valores inconsistentes ou fora do padrão em algumas colunas.

## Correções
Foram realizadas as seguintes correções nos dados:

1.  **Coluna 'Aparencia':**
    -   Identificado um valor incorreto ('menos').
    -   O valor 'menos' foi substituído pela moda da coluna, que era 'sol'.

2.  **Coluna 'Temperatura':**
    -   Identificado um valor anômalo (1220).
    -   O valor anômalo foi substituído pela mediana da coluna 'Temperatura'.

3.  **Coluna 'Umidade':**
    -   Identificado um valor anômalo (200) e também um valor vazio.
    -   O valor anômalo e o campo vazio foram substituídos pela mediana da coluna 'Umidade'.

4.  **Coluna 'Vento':**
    -   Identificado um campo vazio.
    -   O campo vazio foi preenchido com a moda da coluna, que era 'FALSO'.

## Gráficos
Para cada coluna analisada ('Aparencia', 'Temperatura', 'Umidade', 'Vento', 'Jogar'), foram gerados gráficos de barras (`plot.bar()`) para visualizar a distribuição dos dados e boxplots (`sns.boxplot()`) para identificar a presença de outliers. Esses gráficos foram cruciais para a identificação visual das inconsistências antes do tratamento.

## Considerações Finais
Após a análise detalhada e as correções aplicadas, o dataset `tempo.csv` está limpo e consistente, pronto para ser utilizado em etapas subsequentes de análise ou modelagem. Todas as inconsistências identificadas foram tratadas utilizando métodos estatísticos (moda e mediana) para preencher ou corrigir os valores, garantindo a qualidade dos dados.
