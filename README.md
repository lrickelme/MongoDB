```markdown
# Operações CRUD com MongoDB em Python

Este projeto demonstra como realizar operações básicas de CRUD (Criar, Ler, Atualizar, Deletar) utilizando Python e MongoDB. O script interage com coleções do MongoDB para gerenciar dados como times, jogadores e temporadas.

## Funcionalidades

- Carregar dados iniciais de um arquivo JSON no MongoDB.
- Criar um novo registro em uma coleção específica.
- Ler registros de uma coleção com filtros opcionais.
- Atualizar um registro em uma coleção com base em um filtro.
- Deletar um registro de uma coleção com base em um filtro.

## Pré-requisitos

- Python 3.7 ou superior.
- Banco de dados MongoDB.
- Um arquivo `.env` com a variável `URL_MONGODB` configurada com sua string de conexão MongoDB.

## Como Executar

1. Execute o script:

   ```bash
   python inserir_mongoDb.py
   ```

2. O script realizará as seguintes ações:
   - Carregará os dados iniciais do arquivo `results.json` para as coleções `season`, `team` e `player`.
   - Adicionará um novo time à coleção `team`.
   - Recuperará e imprimirá os times de uma cidade específica.
   - Atualizará o apelido de um time.
   - Excluirá um time pelo ID.

## Estrutura dos Arquivos

- **`main.py`**: Contém as operações CRUD e a lógica principal do script.
- **`requirements.txt`**: Lista os pacotes Python necessários.
- **`.env`**: Contém a string de conexão com o MongoDB (não incluído no repositório).

## Requisitos

Os seguintes pacotes Python são utilizados neste projeto:

- `pymongo==4.10.1`
- `python-dotenv==1.0.1`
- `dnspython==2.7.0`

## Exemplo

```python
# Exemplo de registro para inserção na coleção 'team'
novo_time = {
    "id": 1313,
    "full_name": "CG Team",
    "abbreviation": "CGT",
    "nickname": "Campina Grande",
    "city": "CG City",
    "state": "Campeão",
    "year_founded": 2025
}
```

## Observações

- Certifique-se de que o MongoDB está em execução e acessível pela string de conexão.
- Ajuste o arquivo `results.json` para refletir o esquema de dados necessário.
- Implemente tratamentos de exceções para melhor gerenciamento de erros em ambientes de produção.
