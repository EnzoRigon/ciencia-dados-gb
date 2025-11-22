# Projeto GB — Instruções de execução

Resumo rápido
-------------
Este repositório visa classifica um cliente para uma análise de crédito com base em um dataset público. As instruções abaixo explicam como criar um ambiente Python compatível, instalar dependências e abrir o notebook para reproduzir as análises.

Versão do Python
-----------------
Este projeto foi criado e testado com Python 3.13.2. Recomenda-se usar exatamente essa versão quando possível para evitar incompatibilidades.

Requisitos
---------
- Python 3.13.2 (recomendado: usar pyenv ou instalador oficial)
- `pip` e `virtualenv`/`venv`

Instalação (sugestão rápida)
---------------------------
1. Criar e ativar um ambiente virtual (usando venv embutido)

	```bash
	python3.13 -m venv .venv
	source .venv/bin/activate
	```

	Se `python3.13` não existir no PATH, use `python3` ou o caminho fornecido pelo `pyenv` (por exemplo `~/.pyenv/versions/3.13.2/bin/python`).

2. Atualizar pip e instalar dependências

	```bash
	pip install -r requirements.txt
	```
3. Selecionar o interpretador Python da versão que esta no venv

Arquivos importantes
-------------------
- `clean_dataset.ipynb` — notebook principal com análises detalhada e tratativa de dados.
- `data_view.ipynb` — notebook com análise geral sobre os dados, dispersão, outliers, etc.
- `ml.ipynb` — notebook com os algoritmos de classificação da análise de crédito.
- `data.csv` — dataset usado, [disponibilizado no Kaggle](https://www.kaggle.com/datasets/parisrohan/credit-score-classification/data).
- `requirements.txt` — dependências Python (instale com `pip install -r requirements.txt`).

Dicas e resolução de problemas
-----------------------------
- Se faltar pacotes no `requirements.txt`, instale-os com `pip install <package>` e atualize o arquivo com `pip freeze > requirements.txt` (opcional).
- Se tiver erro de versão do Python, confirme a versão ativa com `python --version` ou `python3 --version`.

# Sobre o dataset
-----------------------------
## Dicionário de dados

| Coluna                   | Tipo   | Descrição                                                       | Natureza da Variável                                   |
| ------------------------ | ------ | --------------------------------------------------------------- | ------------------------------------------------------ |
| ID                       | String | Identificador único do dado                                     | Categórica nominal                                     |
| Customer_ID              | String | Identificador do cliente                                        | Categórica nominal                                     |
| Month                    | String | Mês de referência                                               | Categórica ordinal                                     |
| Name                     | String | Nome do cliente                                                 | Categórica nominal                                     |
| SSN                      | String | Social security number do cliente                               | Categórica nominal                                     |
| Age                      | Número | Idade da pessoa                                                 | Numérica discreta                                      |
| Occupation               | String | Profissão da pessoa                                             | Categórica nominal                                     |
| Annual_Income            | Número | Renda anual do cliente                                          | Numérica contínua                                      |
| Monthly_Inhand_Salary    | Número | Salário líquido mensal                                          | Numérica contínua                                      |
| Num_Bank_Accounts        | Número | Quantidade de contas bancárias                                  | Numérica discreta                                      |
| Num_Credit_Card          | Número | Quantidade de cartões de crédito                                | Numérica discreta                                      |
| Interest_Rate            | Número | Taxa média de juros                                             | Numérica contínua                                      |
| Num_of_Loan              | Número | Quantidade total de empréstimos                                 | Numérica discreta                                      |
| Type_of_Loan             | String | Tipos de empréstimo                                             | Categórica nominal                                     |
| Delay_from_due_date      | Número | Dias de atraso                                                  | Numérica discreta                                      |
| Num_of_Delayed_Payment   | Número | Número de pagamentos atrasados                                  | Numérica discreta                                      |
| Changed_Credit_Limit     | Número | Percentual do limite de crédito alterado                        | Numérica contínua                                      |
| Num_Credit_Inquiries     | Número | Quantidade de consultas de crédito                              | Numérica discreta                                      |
| Credit_Mix               | String | Distribuição dos tipos de crédito                               | Categórica ordinal                                     |
| Outstanding_Debt         | Número | Dívida pendente total                                           | Numérica contínua                                      |
| Credit_Utilization_Ratio | Número | Percentual de uso do crédito                                    | Numérica contínua                                      |
| Credit_History_Age       | String | Tempo total de histórico de crédito                             | Categórica ordinal                                     |
| Payment_of_Min_Amount    | String | Indica se o cliente paga o mínimo                               | Categórica ordinal                                     |
| Total_EMI_per_month      | Número | Soma das parcelas mensais                                       | Numérica contínua                                      |
| Amount_invested_monthly  | Número | Total investido mensalmente                                     | Numérica contínua                                      |
| Payment_Behaviour        | String | Padrão de pagamento                                             | Categórica nominal                                     |
| Monthly_Balance          | Número | Saldo médio mensal                                              | Numérica contínua                                      |
| Credit_Score             | String | Classificação do crédito                                        | Categórica ordinal                                     |
