# Gatito Petshop | Dashboard de Vendas no Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black) ![Business Intelligence](https://img.shields.io/badge/Business%20Intelligence-An%C3%A1lise%20Comercial-6F2C91)

## Visão geral

Projeto de **Business Intelligence** com foco na exploração de dados de vendas e clientes de um petshop. O relatório foi desenvolvido no **Microsoft Power BI**, reunindo indicadores comerciais, comparações de faturamento e recursos de segmentação para facilitar a leitura dos resultados.

> **Para recrutadores:** o arquivo [`PowerBI - Pets.pbix`](./PowerBI%20-%20Pets.pbix) está disponível para download e análise no Power BI Desktop. O GitHub não executa arquivos `.pbix` diretamente.

## Perguntas de negócio

- Como o faturamento varia ao longo do tempo?
- Quais bairros concentram maior faturamento?
- Como o faturamento se distribui entre os gêneros cadastrados?
- Qual é a quantidade de itens vendidos?
- Qual é a média de pets por cliente?
- Como marca, período e nome do produto ajudam a segmentar a análise?

## Indicadores e visualizações identificados no relatório

| Elemento | Implementação no PBIX |
| --- | --- |
| Faturamento total | Cartão com medida `Vendas.Faturamento total` |
| Quantidade vendida | Cartão com soma de `Vendas.Quantidade` |
| Média de pets | Cartão com média de `Clientes.Pets` |
| Faturamento por gênero | Gráfico de pizza com `Clientes.Gênero` |
| Faturamento por bairro | Gráfico de barras com `Clientes.Bairro` |
| Evolução do faturamento | Gráfico de área por data de compra, com hierarquia temporal |
| Filtro por marca | Segmentação por `Produtos.Marca` |
| Filtro por data | Segmentação por `Vendas.Data de compra` |
| Pesquisa de produtos | Visual personalizado de filtro por `Produtos.Nome produto` |
| Imagens de produtos | Visual personalizado baseado em `Produtos.Url img` |

Esses elementos foram identificados diretamente na estrutura do arquivo `.pbix`. **Não são apresentados valores de desempenho ou conclusões quantitativas sem validação dos resultados no Power BI Desktop.**

## Tecnologias e recursos

- **Power BI Desktop:** construção do relatório e visualização dos dados.
- **Bases Excel e TXT:** arquivos de entrada disponibilizados neste repositório.
- **Gráficos e segmentações:** comparação de indicadores e filtros de exploração.
- **Visuais personalizados:** ImageGrid e TextFilter, encontrados no arquivo do relatório e disponibilizados separadamente em `visuais/`.

> A presença de Power Query e expressões DAX específicas não foi auditada nesta documentação; consulte o projeto no Power BI Desktop para analisar as etapas e a implementação das medidas.

## Estrutura do repositório

```text
power-bi-gatito-petshop/
├── README.md
├── PowerBI - Pets.pbix
├── dados/
│   ├── Clientes.txt
│   ├── Gatitos_2020.xlsx
│   ├── Gatitos_2021.xlsx
│   ├── Gatitos_2022.xlsx
│   └── Produtos_gatitos.xlsx
├── visuais/
│   ├── ImageGrid.pbiviz
│   └── TextFilter.pbiviz
└── assets/
    └── Gatito.jpg
```

## Como executar

1. Instale o [Power BI Desktop](https://www.microsoft.com/pt-br/power-platform/products/power-bi/desktop).
2. Baixe este repositório em **Code → Download ZIP** e extraia os arquivos.
3. Abra `PowerBI - Pets.pbix` no Power BI Desktop.
4. Se a atualização dos dados solicitar arquivos ausentes, corrija os caminhos de origem para a pasta `dados/` em **Transformar dados → Configurações da fonte de dados** ou nas etapas de origem das consultas.
5. Caso algum visual não seja carregado, reimporte o arquivo correspondente na pasta `visuais/`.
6. Navegue pelos gráficos e experimente os filtros de marca, período e produto.

> A abertura do relatório e a atualização das fontes não foram testadas em uma instalação local do Power BI Desktop neste ambiente. As fontes podem manter caminhos absolutos do computador original.

## Apresentação visual

A identidade visual do projeto utiliza elementos de marca do Gatito Petshop e tons de roxo. Para visualizar **os gráficos preenchidos com dados**, abra o PBIX no Power BI Desktop.

![Identidade visual Gatito Petshop](assets/Gatito.jpg)

## Possíveis análises

A combinação entre faturamento, dimensões de clientes, datas de compra e marcas permite **investigar** concentração geográfica das vendas, evolução temporal e segmentação comercial. Essas são possibilidades analíticas oferecidas pela estrutura do relatório, **não conclusões previamente comprovadas sobre a base**.

## Notas sobre dados e publicação

- As bases são fornecidas para permitir a inspeção do projeto. **Antes de publicar este repositório publicamente, confirme que você possui autorização para divulgar todos os arquivos**, sobretudo `Clientes.txt` e o PBIX, que pode conter dados incorporados.
- Caso sejam dados reais de clientes, considere substituir os arquivos por versões anonimizadas ou sintéticas e revisar os campos e relacionamentos antes da publicação.
- O GitHub hospeda o arquivo `.pbix`, mas não disponibiliza o painel interativo diretamente na página do repositório.

---

**Projeto de portfólio | Power BI · Business Intelligence · Análise de Vendas**
