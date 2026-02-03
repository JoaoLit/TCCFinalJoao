# MRP Varejo Inteligente

Sistema de Planejamento de Necessidades de Materiais (MRP) com análise preditiva e inteligência artificial.

## Funcionalidades

- Cálculo automático de estoque de segurança
- Planejamento mensal (1 a 12 meses)
- Dashboard estratégico com Curva ABC
- Análise de faturamento por ano
- Análise inteligente com IA (OpenAI)
- Gráficos interativos de comportamento de produtos
- Exportação para Excel

## Como usar

1. Faça upload da planilha de vendas (CSV ou Excel)
2. Configure o nível de serviço e lead time
3. Visualize os relatórios mensais e consolidados
4. Exporte os dados em Excel

## Formato da Planilha

A planilha deve conter as seguintes colunas:

- **EMISSAO**: Data da venda
- **CONTAGEM**: Indicador (0 ou 1)
- **ITEM**: Nome/Código do produto
- **GRUPO**: Categoria
- **QUANTIDADE**: Quantidade vendida
- **VALOR**: Valor total da venda
- **CUSTO**: Custo total da transação

## Deploy no Streamlit Community Cloud

1. Faça fork deste repositório
2. Acesse [share.streamlit.io](https://share.streamlit.io)
3. Conecte seu repositório GitHub
4. O app será implantado automaticamente

## Requisitos

Veja `requirements.txt` para lista completa de dependências.

## Análise com IA

Para usar a funcionalidade de análise com IA, você precisa de uma API Key da OpenAI. Obtenha em [platform.openai.com/api-keys](https://platform.openai.com/api-keys).
