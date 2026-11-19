# O que o DRE conta sobre a manutenção?

Dashboard interativo que lê as demonstrações financeiras de uma indústria de base florestal com olhar de analista de manutenção. A pergunta-chave: **o que o DRE revela sobre a manutenção da empresa?**

Estudo independente com dados públicos, para fins educacionais. Não é recomendação de investimento. A empresa não é identificada de propósito: o foco é o método, não a companhia.

## O que o painel mostra

- **Indicadores de manutenção:** despesa de manutenção, manutenção sobre a receita, manutenção sobre depreciação e amortização (D&A), EBITDA ajustado, margem operacional e dívida líquida/EBITDA.
- **Evolução no tempo (1T25 a 3T26):** manutenção, margens, variação anual, EBITDA e caixa operacional, custos financeiros, CAPEX sobre D&A, estoque de peças e desgaste da planta.
- **Filtros:** período (trimestre, acumulado no ano, anual), visão (valor, % da receita, variação % a/a), moeda (US$ ou R$) e tema claro ou escuro.
- **Sete leituras de um analista de manutenção**, cada uma com os números, a interpretação e uma pergunta para a gestão.

## As sete leituras, em uma linha

1. A manutenção foi cortada em 2025, mas não é ela que explica a queda do EBITDA.
2. Manutenção e CAPEX caíram em relação ao desgaste do ativo.
3. Em 2026, menos manutenção ainda não virou mais margem.
4. Cortar 10% da manutenção vale pouco diante do risco de uma parada não programada.
5. A manutenção é sazonal: o início do ano pesa mais.
6. O custo do dinheiro já pesa tanto quanto o custo de manter.
7. O estoque de peças subiu enquanto o gasto de manutenção caiu.

São hipóteses para validar com dados operacionais, não conclusões.

## O que o DRE não conta

Disponibilidade, MTBF, MTTR, horas de parada, custo de falha, backlog de ordens, mão de obra própria (que fica em salários) e componentes capitalizados (que vão para CAPEX). Sem esses dados, qualquer conclusão sobre a eficiência da manutenção é parcial.

## Como usar

Abra o `index.html` no navegador. É um arquivo único, com dados e código embutidos, e funciona sem internet. Para publicar, use o GitHub Pages.

## Método e limites

- **Manutenção** é a linha "Maintenance expenses" da nota de despesas por natureza. Não é o custo total de manutenção.
- **Períodos:** o 4T25 é derivado (ano 2025 menos 1T a 3T). O 1T25 usa a apresentação reapresentada nas demonstrações do 2T26. Somas de trimestres podem diferir do acumulado reportado em até 1 mil, por arredondamento. 2024 só existe como ano.
- **Moeda:** margens e razões são calculadas em US$ e não mudam com a moeda. Em R$, cada trimestre usa a média simples das médias mensais da PTAX de venda; saldos usam a PTAX do último dia do mês. As cotações vêm de sites que republicam dados do Banco Central, conferidos entre fontes, e não de consulta direta à API oficial. A média de set/26 tem fonte única.
- **Dívida líquida/EBITDA** é uma conta simples (dívida financeira menos caixa, sobre o EBITDA ajustado dos últimos 12 meses) e pode diferir da métrica da empresa.
- **Set/26:** uma unidade de embalagens corrugadas foi reclassificada como mantida para venda, o que reduz o estoque de peças e altera a base do desgaste da planta.
- **Associação não é causa.** O painel mostra o que anda junto no tempo, não o que causa o quê.

## Tecnologias

HTML, CSS e JavaScript puros, com [D3](https://d3js.org/) para os gráficos. Cores de gráfico validadas para daltonismo nos temas claro e escuro.

## Autor

Leonardo de Re da Silva · técnico de manutenção em transição para análise de dados · [LinkedIn](https://www.linkedin.com/in/leonardosilvars)
