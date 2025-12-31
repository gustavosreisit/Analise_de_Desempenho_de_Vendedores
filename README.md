# Analise_de_Desempenho_de_Vendedores
Pipeline ETL de análise de desempenho de vendedores utilizando Google Sheets (extração), SQLite/SQL (transformação) e Power BI (visualização), com foco em métricas de vendas e metas.

Análise de Desempenho de Vendedores — Pipeline ETL com SQL

📌 Visão Geral do Projeto

Este projeto tem como objetivo demonstrar, na prática, o processo completo de ETL (Extract, Transform, Load) aplicado a um cenário real de análise de desempenho comercial.

Os dados representam informações mensais de vendas por colaborador, incluindo metas, situação (meta batida ou não) e indicadores consolidados para análise de produtividade.

O foco do projeto é evidenciar habilidades em organização de dados, tratamento com SQL e preparação para visualização em ferramentas de BI.
---

🔹 Extract (Extração dos Dados)

A etapa de extração foi realizada a partir do Google Sheets, simulando uma fonte de dados comum no ambiente corporativo.

Durante essa etapa, foram aplicadas boas práticas como:

Estruturação dos dados em formato tabular

Padronização de colunas (colaborador, mês, vendas, meta, situação)

Ajuste de localidade para garantir compatibilidade numérica (formato internacional)

Exportação dos dados em formato CSV, garantindo fácil integração com bancos relacionais

Essa abordagem reflete cenários reais em que dados operacionais são inicialmente registrados em planilhas antes de serem integrados a sistemas analíticos.
---

🔹 Transform (Transformação dos Dados no SQLite)

A etapa de transformação foi realizada utilizando SQLite e SQL, com foco na limpeza, validação e análise dos dados.

Principais atividades realizadas nesta fase:

Importação do CSV para um banco SQLite

Definição e validação dos tipos de dados (INTEGER, REAL, TEXT)

Identificação de valores nulos (NULL) em colunas críticas, como meta_mensal

Tratamento de inconsistências nos dados para garantir comparações corretas

Criação de consultas SQL para responder perguntas de negócio, como:

Quantas vezes cada colaborador bateu a meta?

Qual o desempenho por mês?

Quem são os colaboradores mais produtivos no período?
---

Exemplo de transformação aplicada:

UPDATE Analise_de_Desempenho_de_Vendedores

SET meta_mensal = 5000

WHERE meta_mensal IS NULL;

<img width="893" height="617" alt="image" src="https://github.com/user-attachments/assets/3aefded0-27e0-41a7-a0f8-622ee4721c0e" />



Além disso, foram desenvolvidas queries agregadas para geração de métricas que serão utilizadas diretamente nas visualizações.
---
🔹 Load (Carregamento no Power BI)

Após o tratamento e consolidação dos dados no SQLite, o próximo passo do projeto consiste no carregamento dos dados no Power BI.

Objetivos desta etapa:

Conectar o Power BI ao banco SQLite

Criar dashboards analíticos com foco em desempenho comercial

Desenvolver KPIs como:

Total de vendas

Quantidade de metas batidas por colaborador

Comparação de desempenho mensal

Aplicar boas práticas de visualização e storytelling com dados

Essa etapa completa o pipeline ETL, transformando dados tratados em insights visuais e acionáveis.

🛠️ Tecnologias Utilizadas

Google Sheets — Organização inicial e extração dos dados

SQLite — Armazenamento e transformação dos dados

SQL — Análise, limpeza e agregação das informações

Power BI — Visualização de dados e criação de dashboards (em desenvolvimento)

🎯 Considerações Finais

Este projeto faz parte do meu portfólio como Analista de Dados, demonstrando domínio do processo ETL, tratamento de dados com SQL e preparação de bases para ferramentas de Business Intelligence.

O fluxo adotado reflete situações reais encontradas em ambientes corporativos, desde planilhas operacionais até dashboards executivos.
