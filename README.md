# SANEAMENTO COMO POLÍTICA DE ADAPTAÇÃO CLIMÁTICA: UMA ANÁLISE DOS DESDOBRAMENTOS NA SAÚDE EM PERNAMBUCO NO PERÍODO DE 2002 E 2021

Este repositório contém os dados e códigos para o projeto de pesquisa que investiga a eficácia da infraestrutura de saneamento básico como uma política de adaptação aos impactos de eventos de chuva extrema na saúde pública. O estudo utiliza um painel de dados em nível municipal para os 185 municípios do estado de Pernambuco, cobrindo o período de 2002 a 2021.

## Visão Geral
A literatura de economia do clima já estabeleceu que os danos de choques climáticos se concentram desproporcionalmente em populações vulneráveis . Este projeto investiga se a infraestrutura de saneamento básico funciona como uma tecnologia de resiliência, protegendo o capital humano desses impactos. A pesquisa se aprofunda na análise dos efeitos de chuvas extremas, um risco climático recorrente e de grande impacto em Pernambuco, sobre diversos desfechos de saúde. O objetivo é ir além da comprovação de um efeito médio, buscando entender como, onde e sob quais condições essa proteção se manifesta.

## Problema de Pesquisa
A questão central da pesquisa, refinada após uma análise exploratória inicial (MVP), é:

Qual a natureza e a magnitude do efeito protetor da infraestrutura de saneamento básico contra os impactos de saúde de eventos de chuva extrema nos municípios de Pernambuco, e como essa eficácia é moderada por diferentes mecanismos epidemiológicos, contextos socioespaciais e dinâmicas temporais?

## Estratégia Empírica
A estratégia de identificação causal se baseia em um 

modelo de painel com Efeitos Fixos de Duas Vias (TWFE), que controla por características não observáveis e constantes no tempo de cada município, bem como por choques anuais comuns a todo o estado . A análise se desdobra em múltiplas fases, incluindo:

- Estimação do Modelo de Referência: Para testar o efeito protetor base.

- Testes de Robustez: Alterando sistematicamente as definições das variáveis de choque climático e de saneamento.

- Análise de Mecanismos: Replicando o modelo para diferentes desfechos de saúde (Leptospirose, Arboviroses, Esquistossomose, etc.), cada um com uma via de transmissão distinta.

- Análise de Heterogeneidade: Estimando o modelo em subamostras de municípios (por densidade populacional) e em subperíodos para investigar a variação do efeito no espaço e no tempo.

## Fontes de Dados
O painel de dados foi construído a partir das seguintes fontes públicas:

- Saúde: Taxas de incidência/internação por 100 mil habitantes, obtidas do DATASUS (SINAN).

- Choque Climático: Variáveis de frequência e intensidade de chuvas extremas, calculadas a partir dos dados diários do dataset 'Zonal BR-DWGD'.

- Saneamento: Séries anuais de cobertura de água e esgoto, construídas a partir dos dados dos Censos de 2000, 2010 e 2022 (IBGE/SIDRA) e tratadas com interpolação.

- Controles: PIB per capita, População e Área dos municípios (IBGE).

## Estrutura do Repositório
O projeto está organizado em duas pastas principais para garantir a reprodutibilidade:

/build: Contém os scripts e dados para a construção da base de dados final.

/input/: Armazena os dados brutos.

/code/: Notebooks para limpeza, tratamento e junção dos dados.

/output/: Armazena os arquivos de dados intermediários e o painel de dados final e limpo.

/analysis: Contém os scripts e resultados da análise.

/input/: Recebe o painel de dados final gerado pela pasta build.

/code/: Notebooks para a análise descritiva e a estimação dos modelos econométricos.

/output/: Armazena as tabelas, gráficos e mapas gerados.

## Estado Atual do Projeto

A fase de build (construção da base de dados) foi concluída, e uma análise econométrica inicial (MVP) foi realizada. Os principais achados exploratórios que guiam a fase atual de analysis são:

O efeito protetor do saneamento é heterogêneo. A eficácia varia dependendo do tipo de doença analisada e do componente de saneamento (água vs. esgoto).

O contexto demográfico importa. O efeito protetor se mostrou estatisticamente significativo apenas em subgrupos específicos de municípios (ex: áreas de alta densidade para a leptospirose).

A relação não é estável no tempo. A análise em subperíodos sugere que a força do efeito protetor pode ter diminuído nos anos mais recentes.

O trabalho atual na pasta analysis se concentra em formalizar e testar a robustez desses achados.
