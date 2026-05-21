# Monitoramento de Atendimentos SAC

## Sobre o projeto

Este projeto foi desenvolvido com o objetivo de simular um dashboard de monitoramento de atendimentos de SAC, utilizando Power BI para transformar dados operacionais em informações visuais e de fácil interpretação.

A proposta do dashboard é acompanhar indicadores importantes da área de atendimento ao cliente, como volume de atendimentos, nível de satisfação, tempo médio de chamada e tempo médio de espera. Com isso, é possível identificar padrões, gargalos e oportunidades de melhoria no processo de atendimento.

---

## Link de visualização

[Visualizar dashboard no Power BI](https://app.powerbi.com/view?r=eyJrIjoiNmJhNmEyNzEtOWI0ZC00NjM1LTkyMmMtZjZmOGVkYTgwZDc3IiwidCI6ImQyOGM4ZWMxLTQ2OTMtNDY5ZS1hMTg4LTkyOTkwNzU1NWNhMSJ9)

---

## Tecnologias utilizadas

- Power BI
- DAX
- Power Query
- ETL
- SQL
- Excel
- GitHub

---

## Estrutura do repositório

| Pasta | Descrição |
|---|---|
| `dados/` | Contém a base de dados utilizada no projeto. |
| `powerbi/` | Contém o arquivo `.pbix` do dashboard. |
| `imagens/` | Contém imagens e prints do dashboard. |
| `full project/` | Contém o projeto completo compactado para download. |

---

## Indicadores analisados

O dashboard foi construído para acompanhar os principais indicadores relacionados ao atendimento ao cliente, incluindo:

- Total de atendimentos realizados
- Média do índice de satisfação dos clientes
- Tempo médio de duração das chamadas
- Tempo médio de espera na ligação
- Evolução dos atendimentos ao longo do tempo
- Análise geral do desempenho do SAC

---

## Medidas DAX utilizadas

| Medida | Fórmula DAX | Objetivo |
|---|---|---|
| Calendário | `dCalendário = CALENDAR(MIN(Fonte[Data]), MAX(Fonte[Data]))` | Cria uma tabela calendário com datas sequenciais entre a menor e a maior data da base. |
| Total de atendimentos | `Numero de atendimentos = COUNTROWS(Fonte)` | Conta o total de atendimentos registrados na base de dados. |
| Média de satisfação | `media = AVERAGE(Fonte[Índice de Satisfação])` | Calcula a média do índice de satisfação dos clientes. |
| Média de duração da chamada | `Medida = AVERAGE(Fonte[Duração de Chamada]) / 60` | Calcula o tempo médio de duração das chamadas em minutos. |
| Média de espera na ligação | `tempo media = AVERAGE(Fonte[Tempo de Espera em Segundos]) / 60` | Calcula o tempo médio de espera dos clientes em minutos. |

---

## Tratamento dos dados

Antes da construção do dashboard, os dados passaram por etapas de tratamento e organização para melhorar a qualidade da análise.

Entre os principais processos realizados estão:

- Ajuste dos tipos de dados
- Organização da base para análise no Power BI
- Criação de tabela calendário
- Padronização de campos
- Criação de medidas DAX
- Conversão de tempos para facilitar a leitura dos indicadores
- Estruturação dos dados para construção dos visuais
