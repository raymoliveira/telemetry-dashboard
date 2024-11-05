# Dashboard de Transmissão de Dados de Telemetria

Este repositório contém um exemplo de dashboard desenvolvido em Power BI para monitorar a transmissão de dados de equipamentos de telemetria. Este projeto é baseado em dados fictícios e simula as funcionalidades de monitoramento e análise da qualidade de transmissão em tempo real.

## Objetivo do Projeto

O objetivo é fornecer uma visão centralizada e D-1 da transmissão de dados dos equipamentos de telemetria, permitindo acompanhar taxas de sucesso, frequência de transmissão, e identificar períodos de falha. Esse tipo de dashboard auxilia na tomada de decisão rápida e garante a confiabilidade dos dados recebidos.

## Estrutura do Projeto

1. **Coleta de Dados**: Monitoramento de dados transmitidos por equipamentos de telemetria, simulados aqui com dados fictícios.
2. **Transformação de Dados**: Aplicação de processos de ETL no Power Query para garantir a consistência dos dados recebidos.
3. **Cálculos e Métricas (DAX)**:
   - **Taxa de Sucesso da Transmissão**: Percentual de transmissões bem-sucedidas em relação ao total.
   - **Frequência de Transmissão**: Média de transmissões por intervalo de tempo.
   - **Período de Falha**: Identificação dos momentos em que não há transmissão de dados.
4. **Visualizações Interativas**: Gráficos e indicadores que permitem monitorar o status da transmissão e analisar padrões de dados ao longo do tempo.

## Tecnologias Utilizadas

- **Power BI**: Visualização e análise de dados.
- **DAX (Data Analysis Expressions)**: Linguagem para cálculos e agregações.
- **Power Query**: Limpeza e transformação dos dados.

## Visualizações

![Visão Geral do Dashboard](mockups/overview.png)
![Status de Transmissão](mockups/transmission_status.png)

## Exemplo de Cálculos em DAX

Aqui estão alguns exemplos de medidas DAX usadas no projeto:

- **Taxa de Sucesso da Transmissão**:
  ```DAX
  Taxa_Sucesso = 
      DIVIDE(COUNTROWS(Filtrado[Transmissões_Sucesso]), COUNTROWS(Tabela[Transmissões]), 0)
