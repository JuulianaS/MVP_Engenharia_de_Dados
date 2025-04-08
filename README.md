# Análise do Mercado de Medicamentos no Tratamento do Câncer de Próstata: Tendências e Previsões de venda

Este projeto tem como objetivo analisar tendências de mercado e prever a demanda futura de medicamentos utilizados no tratamento de câncer de próstata no Brasil, com foco em casos metastáticos. A análise foi realizada com dados dos últimos 24 meses e implementada em um pipeline de dados na nuvem utilizando a plataforma *Databricks Community Edition, integrando com **Power BI* para visualizações interativas.

---

## 1. Objetivo

Analisar o mercado de medicamentos para câncer de próstata no Brasil, utilizando modelagem em camadas (Bronze, Silver e Gold), estrutura em esquema estrela e técnicas de machine learning para previsão de demanda.

---

## 2. Pipeline de Dados

- *Bronze Layer*: Ingestão dos arquivos brutos (CSV).
- *Silver Layer*: Limpeza, transformação e estruturação em modelo dimensional (esquema estrela).
- *Gold Layer*: Dados prontos para consumo analítico, incluindo previsões de vendas.

---

## 3. Modelagem Dimensional

O modelo segue um *esquema estrela*, com a seguinte estrutura:

### Tabela Fato:
- fato_vendas: Contém as métricas de vendas por período, local e produto.

### Tabelas Dimensão:
- dim_produto: Detalhes dos medicamentos.
- dim_local: Informações geográficas e canais de venda.

> Veja o diagrama de dados na pasta [3_Screenshot_Diagrama_Estrela.jpg](Diagrama_Estrela).

---

## 4. Previsões

Utilizou-se o modelo *GBTRegressor* para prever as vendas futuras (fev/2025 a dez/2025). Um ajuste manual foi feito para *jul/2025*, utilizando a média de jun e ago/2025, devido a um pico atípico identificado na projeção.

---

## 5. Visualizações

As análises foram desenvolvidas no *Power BI* e incluem:

- Tendência histórica vs previsão
- Ranking por UF, cidade e canal
- Análise por tipo de medicamento
- Participação nacional vs internacional

---

## 6. Autoavaliação

As etapas foram concluídas com sucesso. Dificuldades enfrentadas envolveram:

- Implementação do modelo de previsão no ambiente limitado do Databricks Community
- Tratamento de anomalias nas projeções
- Exportação do arquivo final em CSV para Power BI

---

## 7. Documentação Completa

O documento completo com todas as respostas do MVP, justificativas técnicas, decisões de modelagem e prints está disponível no link abaixo:

[📄 Acesse aqui o documento em PDF](1_Analise_e_processos_realizados_documentação.pdf)

---

## 8. Tecnologias Utilizadas

- *Databricks Community Edition*
- *Apache Spark (PySpark)*
- *Power BI*
- *Python*
- *CSV / DBFS*

---

## 9. Autora

Desenvolvido por Juliana Silva 
Analista de Business Intelligence | IQVIA
