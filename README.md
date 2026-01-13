# Transformação de Dados & Dashboard: Análise Pet-Shop

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logo=microsoft&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

Projeto completo de Governança de Dados desenvolvido durante formação técnica em Ciências de Dados, transformando uma base de vendas crítica em dashboards interativos para tomada de decisão estratégica.

---

## O Desafio

Base de dados de vendas de pet-shop com 250.062 linhas e 16 colunas apresentando múltiplos problemas de qualidade:

- Todas colunas em tipo texto (incluindo números e datas)
- Colunas sem nomenclatura adequada
- Outliers negativos e valores zerados
- Datas inválidas (ex: 31 de fevereiro)
- Dados de teste não removidos ("teste", "qtd x")
- Inconsistências de padronização (Norte vs "noRtE")
- Regiões com estados incorretos
- Valores faltantes em colunas críticas
- Problemas de locale (ponto vs vírgula em decimais)

---

## A Solução

Transformação de Dados (Power Query)

Padronização:
- Promoveu cabeçalhos e padronizou nomenclatura (ds_nome_coluna)
- Converteu 16 colunas para tipos de dados corretos
- Mesclou colunas DIA + MÊS + ANO em data unificada

Limpeza:
- Corrigiu datas inválidas com cálculo manual (31/02/2020 → 02/03/2020)
- Removeu valores negativos (quantidade e valores não podem ser negativos)
- Substituiu zeros e missings por médias calculadas
- Tratou problemas de locale (decimal com vírgula)
- Limpou registros de teste

Enriquecimento:
- Criou colunas calculadas para recuperar dados faltantes
- Aplicou lógica reversa: total ÷ valor_unitário = quantidade

Manipulação de Dados (DAX)

- Função SWITCH para corrigir estados em regiões erradas
- Medidas customizadas (COUNTROWS)
- Colunas condicionais para análise

---

## Resultado

3 Dashboards Interativos

Dashboard 1 - Maiores Vendas:
- Evolução temporal por mês
- Categoria mais vendida (treemap)
- Top produtos por valor e lucro líquido
- Análise de sazonalidade

Dashboard 2 - Performance de Vendedores:
- Ranking por vendas, comissão e lucro
- Funcionário do mês em destaque
- Relação valor bruto × lucro líquido (scatter plot)
- Identificação de outliers visuais

Dashboard 3 - Análise Geográfica:
- Mapas coropléticos de vendas e lucro por estado
- Comparativo: estado com maior lucro vs maior volume
- Top 5 lojas mais lucrativas
- Identificação de oportunidades regionais

Funcionalidades

- Filtros interativos: ano, mês, produto, categoria, região
- 7 tipos de visualizações (treemap, linhas, dispersão, mapas, barras, tabelas, cards)
- Cross-filtering entre páginas
- KPIs dinâmicos

---

## Insights & Tomada de Decisão

Os dashboards permitem identificar:

- Regiões com baixo desempenho para campanhas direcionadas
- Produtos mais lucrativos para ajuste de estoque
- Vendedores destaque para reconhecimento e benchmarking
- Padrões sazonais para planejamento estratégico

---

## Arquivos do Projeto

- dash_petshop.pbix - Dashboard completo Power BI (dados + transformações + visualizações)
- documentacao_petshop.pdf - Documentação técnica detalhada com metodologia e prints
- base_vendas_petshop.csv - [Link para base de dados original no drive para download](https://drive.google.com/file/d/1YDjMoSVvkfCs2lICCcQExGsKW4ACvIdN/view?usp=drive_link)

  A base de dados utilizada é fictícia e, pelo seu tamanho, não poderá ser acessada diretamente pelo repositório, sendo necessário o download pelo link acima.

---

## Para reproduzir o projeto:

1. Baixe a base de dados original
2. Abra o arquivo `dash_petshop.pbix` no Power BI
3. Abra o editor do Power Query
4. Edite a primeira etapa de edição (Fonte) e selecione o caminho para a base baixada

---

## Tecnologias Utilizadas

- Power BI - Plataforma de visualização e análise
- Power Query - Transformação e limpeza de dados
- DAX - Linguagem de manipulação e cálculos
- Governança de Dados - Metodologia aplicada

---

## Diferenciais do Projeto

- Documentação técnica completa seguindo metodologia formal
- Dicionário de dados antes/depois do tratamento
- Justificativas técnicas para cada decisão
- Tratamento de 250k+ linhas com múltiplos problemas de qualidade
- 3 dashboards temáticos com narrativas distintas

---

## Contato

Diogo Zoboli
e-mail: zobolidiogo@gmail.com
LinkedIn: [linkedin.com/in/zobolidiogo](https://www.linkedin.com/in/zobolidiogo/)

---

Se este projeto foi útil, considere dar uma estrela no repositório!
