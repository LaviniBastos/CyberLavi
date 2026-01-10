---
layout: post
title: "Análise de Dados com SQL — Layoffs Globais"
date: 2026-01-10 12:01:00 +0000
categories: [Analytics, Dados, Análise de dados, Projeto Portifolio ]
tags: [Data Analytics, SQL, Banco de dados ]
description: "Projeto parte do bootcamp 'Data Analytics' utilizando a linguagem SQL para extrair, limpar, manipular e padronizar um conjunto de dados armazenados em um banco de dados."
image: /assets/img/cloud/SQL.png
---

# Objetivo do Projeto

O objetivo deste projeto é realizar uma **análise exploratória de dados (EDA)** a partir de um dataset global de demissões, utilizando SQL como ferramenta principal.  
Antes da análise, foi necessário um processo completo de **limpeza e padronização dos dados**, garantindo consistência e confiabilidade nos resultados.

---
##  Etapa 1 — Preparação e Importação dos Dados

- Criação de um banco de dados no **SQL Workbench**
- Importação do arquivo CSV para o banco
- Inicialmente, os campos de data foram mantidos como texto para permitir tratamento posterior
    
---
## Etapa 2 — Limpeza dos Dados

### 1️. Preservação dos dados brutos

Foi criada uma **tabela de staging**, permitindo que os dados originais permanecessem intactos enquanto o tratamento ocorria em uma cópia.

---
### 2️. Remoção de duplicatas

- O dataset não possuía um identificador único
- Foi criada uma coluna auxiliar utilizando `ROW_NUMBER()` particionando **todas as colunas**
- Isso evitou falsos positivos de duplicatas (ex.: empresa “Oda”)
- Após validação, apenas uma das duplicatas foi removida
- Para permitir a exclusão, foi criada uma terceira tabela com a coluna `row_num`
- O modo _safe update_ foi temporariamente desativado
    

**Insight técnico:** identificar duplicatas exige entendimento do contexto dos dados, não apenas da estrutura ou como eles se apresentam.

---

### 3️. Padronização dos dados

- Uso de `TRIM()` para remover espaços em branco
- Padronização de nomes inconsistentes (maiúsculas/minúsculas)
- Correção de variações na coluna `industry` (ex.: múltiplos registros de “Crypto”)
- Tratamento da coluna `country`, removendo caracteres indevidos como ponto final
- Conversão e padronização de campos de data para permitir análise temporal

---
### 4️. Tratamento de valores nulos

- Identificação de campos vazios na coluna `industry`
- Preenchimento com base em registros existentes da mesma empresa (ex.: Airbnb → Travel)
- Uso de `JOIN` para reaproveitamento de informações consistentes
- Colunas com alto volume de nulos (`total_laid_off`, `percentage_laid_off`) foram removidas quando não impactavam a análise

---
##  Etapa 3 — Análise Exploratória de Dados (EDA)

### Impacto das demissões

- O maior número registrado de demissões em um único evento foi **12.000**
    
- Empresas com `percentage_laid_off = 1` indicam demissão de 100% dos funcionários, sugerindo falência
    

---
### Demissões por empresa

- Amazon lidera o ranking de demissões totais
- Google aparece em segundo lugar
    

---
### Demissões por setor

- Os setores **Consumer** e **Retail** concentram o maior volume de layoffs
- Indicando forte impacto em setores ligados ao consumo e varejo, sendo os mais sensíveis à crises econômicas.

---

### Demissões por país

- Estados Unidos lideram o ranking
- Índia aparece em segundo lugar
- Brasil ocupa a 5ª posição

---

### Análise temporal

- O ano de **2022** apresentou o maior volume de demissões
- Os dados de 2023 abrangem apenas três meses, indicando tendência de crescimento
- Análise de demissões acumuladas mostrou que:
    - 2021 teve crescimento mais estável
    - 2022 apresentou aceleração significativa
        

---

### Ranking anual

- Utilização de CTEs para ranquear empresas que mais demitiram por ano
- Extração das **Top 5 empresas por ano**
- Permite comparações temporais e análise de comportamento corporativo

---

## Conclusão

Este projeto demonstra a aplicação prática de SQL em um cenário real de análise de dados, abordando desde a limpeza até a extração de insights.  
Além do domínio técnico, o projeto reforça a importância da **interpretação crítica dos dados** para apoiar análises econômicas e de mercado.
