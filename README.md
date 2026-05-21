## Projeto com o intuito de monstrar e simular como seria uma dashboard de atendimento ao cliente SAC:
---
### [Link de visualização nativo do Power BI](https://app.powerbi.com/view?r=eyJrIjoiNmJhNmEyNzEtOWI0ZC00NjM1LTkyMmMtZjZmOGVkYTgwZDc3IiwidCI6ImQyOGM4ZWMxLTQ2OTMtNDY5ZS1hMTg4LTkyOTkwNzU1NWNhMSJ9)
---
### Tecnologias usadas:
- Power Bi
- DAX
- ETL
- SQL
- EXCEL
- GITHUB
---
## Medidas DAX utilizadas

| Medida | Fórmula DAX | Objetivo |
|---|---|---|
DCalendario | dCalendário=CALENDAR(MIN(Fonte[Data]),MAX(Fonte[Data]))| Faz com que as datas se organizem de forma sequencial, facilitando a leitura e organização
Total de atendimentos | Numero de atendimentos = COUNTROWS(Fonte)| Executa todos atendimentos feitos na fonte de dados
Média de atendimentos | media = AVERAGE(Fonte[Índice de Satisfação])| Executa a média de atendimentos feitas
Média de duração de atendimento telefônico |Medida = AVERAGE(Fonte[Duração de Chamada]) / 60| Mapea o tempo de ligação média de um atendimento
Média de espera na ligação | tempo media = AVERAGE(Fonte[Tempo de Espera em Segundos Multiplicar por 86.400 dia tem isso de segundos]) / 60| Calcula a média de fila de espera de cada cliente.



