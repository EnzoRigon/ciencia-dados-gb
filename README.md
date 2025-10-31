# Projeto GB — Instruções de execução

Resumo rápido
-------------
Este repositório contém um notebook de análise (`analysis.ipynb`) e um arquivo de dados (`data.csv`). As instruções abaixo explicam como criar um ambiente Python compatível, instalar dependências e abrir o notebook para reproduzir as análises.

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
- `analysis.ipynb` — notebook principal com análises e plots.
- `data.csv` — dataset usado pelo notebook.
- `requirements.txt` — dependências Python (instale com `pip install -r requirements.txt`).

Dicas e resolução de problemas
-----------------------------
- Se faltar pacotes no `requirements.txt`, instale-os com `pip install <package>` e atualize o arquivo com `pip freeze > requirements.txt` (opcional).
- Se tiver erro de versão do Python, confirme a versão ativa com `python --version` ou `python3 --version`.

# ESSE É SÓ UM ESQUELETO