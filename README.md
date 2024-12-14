# DB Atbasica - ETL para Painéis Power BI

## Descrição

Este repositório apresenta um projeto completo de ETL (Extração, Transformação e Carga) desenvolvido para otimizar a coleta, tratamento e centralização de dados da Atenção Básica em Saúde. A solução tem como foco alimentar painéis analíticos no Power BI com informações transformadas e organizadas em um banco de dados PostgreSQL. O pipeline, implementado em Python, integra-se a diversas fontes de dados e aplica transformações para atender aos requisitos de visualização.

## Funcionalidades

- **Extração de Dados**:
  - Coleta de informações de múltiplas fontes, incluindo Google Sheets, SharePoint e arquivos Excel.
  
- **Transformação**:
  - Normalização e integração de tabelas.
  - Conversão para um modelo de dados consistente.

- **Carga**:
  - Armazenamento de dados transformados em um banco de dados PostgreSQL.
  - Estruturação em schemas específicos para organização eficiente.

- **Integração com Power BI**:
  - Disponibilização de dados centralizados para atualizações dinâmicas dos painéis analíticos.

## Estrutura do Projeto

A organização do projeto está dividida em módulos claros para facilitar a manutenção e expansão:

- **`src`**: Contém os códigos principais do pipeline.
  - **`data_processing`**: Scripts para extração e transformação de dados.
    - Exemplo: `asu.py`, `atendimentos.py`.
  - **`database`**: Configuração e conexão com o PostgreSQL.
  - **`sql_operations`**: Scripts para criação de schemas e outras operações SQL.
  - **`utils`**: Funções auxiliares para manipulação de APIs, arquivos e chaves primárias.

- **`scripts_main`**: Scripts de inicialização do processo ETL.
  - **`main.py`**: Gerenciador principal do pipeline.

- **`scripts_sql/transformacoes`**: Repositório de transformações SQL personalizadas utilizando DuckDB.

## Tecnologias Utilizadas

O projeto utiliza tecnologias robustas e modernas para garantir eficácia e escalabilidade:

- **Python**: Base para desenvolvimento do pipeline ETL.
- **PostgreSQL**: Banco de dados relacional para armazenamento estruturado.
- **DuckDB**: Ferramenta leve para manipulações intermediárias.
- **Poetry**: Gerenciador de dependências e ambientes Python.
- **pyenv**: Controle de versões do Python.
- **Google Sheets API e SharePoint API**: Extração direta de dados de fontes online.

## Instalação

1. **Clone o repositório**:

   ```bash
   git clone https://github.com/vinisique/atencao-basica-db.git
   cd atencao-basica-db
   ```

2. **Configure o ambiente Python**:

   ```bash
   pyenv install 3.12.0
   pyenv local 3.12.0
   poetry install
   ```

3. **Configure o Banco de Dados**:

   - Certifique-se de que o PostgreSQL está instalado e rodando.
   - Crie as tabelas e schemas utilizando os scripts em `src/sql_operations`.

## Execução do Projeto

1. Configure as credenciais para acessar o Google Sheets e SharePoint nas variáveis de ambiente ou arquivos de configuração.
2. Execute o pipeline utilizando o script principal:

   ```bash
   poetry run python scripts_main/main.py
   ```

## Exemplos de Visualizações

Os painéis Power BI gerados oferecem insights detalhados sobre:

- Indicadores de saúde.
- Cobertura da atenção básica por região.
- Tabelas dinâmicas e dashboards interativos.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request com melhorias e novas funcionalidades.

## Contato

Para quaisquer dúvidas ou sugestões, entre em contato:

- GitHub: [vinisique](https://github.com/vinisique)
- Email: seuemail@example.com

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

