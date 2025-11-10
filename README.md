# Busca CNPJ

![alt text](image.png)
Aplicação simples em Python + Streamlit que consulta dados de empresas pelo CNPJ usando a BrasilAPI.

## Sobre

Este projeto fornece uma interface web minimalista para buscar informações de um CNPJ (Cadastro Nacional da Pessoa Jurídica) consultando a API pública da BrasilAPI. A interface permite inserir um CNPJ (com ou sem formatação) e exibe os dados retornados, como razão social, nome fantasia, endereço, sócios e atividades.

## Funcionalidades

- Inserir CNPJ (aceita CNPJ com pontos, barras e traço ou apenas números).
- Formatação automática de CNPJ e CEP na exibição.
- Exibição de: razão social, nome fantasia, capital social, data de abertura, telefones, endereço, CEP, e-mail, situação cadastral, regime tributário, sócios e atividades.
- Usa a BrasilAPI (sem necessidade de chave/API key).

## Requisitos

- Python 3.8 ou superior
- Conexão com a internet (consulta a BrasilAPI)

Dependências principais:

- streamlit
- requests

## Instalação (Windows - cmd.exe)

1. Crie e ative um ambiente virtual (recomendado):

```cmd
python -m venv venv
venv\Scripts\activate
```

2. Atualize pip e instale dependências:

```cmd
pip install --upgrade pip
pip install streamlit requests
```

Se preferir, você pode criar um `requirements.txt` contendo `streamlit` e `requests` e instalar com `pip install -r requirements.txt`.

## Como rodar

Execute o Streamlit apontando para o arquivo principal (`main.py`):

```cmd
streamlit run main.py
```

Isso abrirá a interface web no navegador (normalmente em http://localhost:8501). Na página, digite o CNPJ no campo e clique em "Buscar".

## Uso

- Informe o CNPJ completo (ex.: `12.345.678/0001-90` ou `12345678000190`).
- Se o CNPJ estiver correto e presente na base da BrasilAPI, os dados serão exibidos na página.
- Mensagens de erro aparecerão se o CNPJ for inválido (não tiver 14 dígitos) ou se houver problema na conexão com a API.

## Estrutura do projeto

- `main.py` — aplicação Streamlit que realiza a busca e renderiza a interface.
- `pyproject.toml` — metadados do projeto (opcional).
- `README.md` — este arquivo.

## Observações

- A aplicação depende da disponibilidade da BrasilAPI. Em caso de instabilidade ou mudanças na API, algumas informações podem deixar de ser retornadas.
- Não há tratamento de autenticação porque a BrasilAPI usada aqui não exige chave.

## Contribuições

Projeto feito por @mvgentil
https://github.com/mvgentil/busca-cnpj


