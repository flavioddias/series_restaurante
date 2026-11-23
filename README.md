# Previsão de demanda em restaurantes

Análise de séries temporais para estimar o número diário de clientes de dois restaurantes e apoiar o planejamento de insumos e equipes. O projeto explora padrões semanais e produz uma previsão de **14 dias**.

[Explore o notebook](An%C3%A1lise%20de%20s%C3%A9ries%20temporais_restaurantes.ipynb)

## Dados e abordagem

O histórico analisado contém 478 dias, de janeiro de 2016 a abril de 2017, para os restaurantes Chimi & Churri e Assa Frão.

- Tratamento de ausências por interpolação.
- Distribuições, evolução temporal, agregações mensais e média móvel de sete dias.
- Exploração de datas comemorativas, decomposição sazonal e anomalias.
- Gráficos de autocorrelação e autocorrelação parcial.
- Suavização exponencial com sazonalidade aditiva de período sete.
- Visualização das projeções e exportação da tabela para Excel.

O ajuste usa o histórico disponível. Os **últimos 100 dias são a janela de visualização**, não o tamanho do conjunto usado para ajustar o modelo.

## Como explorar e executar

1. Abra o notebook no Jupyter ou Google Colab.
2. Disponibilize `clientes_restaurantes.csv` e `datas_comemorativas.csv`. Esses arquivos **não estão incluídos no repositório**.
3. Ajuste os caminhos que atualmente apontam para o Google Drive.
4. Instale as bibliotecas:

```bash
pip install pandas numpy scipy statsmodels matplotlib plotly openpyxl jupyter
```

5. Adapte a configuração de idioma `pt_BR.utf8` ao seu sistema e execute as células em sequência. Chamadas antigas de frequência mensal podem exigir atualização conforme a versão do pandas.

## Entregas e avaliação

O notebook gera gráficos históricos e uma planilha com as previsões dos próximos 14 dias. A aplicação pretendida é antecipar necessidades operacionais; não há medição de economia ou melhoria operacional no projeto.

A versão publicada **ainda não apresenta backtesting nem métricas de erro fora da amostra**. Para avaliar a utilidade da previsão, os próximos passos são separar períodos temporais, comparar com uma previsão sazonal simples e medir MAE/RMSE. Também é necessário disponibilizar os dados e registrar as versões das dependências.

**Competências demonstradas:** séries temporais, preparação de dados, sazonalidade, visualização e comunicação de aplicações de negócio.
