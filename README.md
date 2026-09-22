Processando e Transformando Dados com Power BI e MySQL na Azure

Projeto desenvolvido como desafio de projeto da trilha de Análise de Dados da DIO.

O objetivo é aplicar, na prática, um fluxo completo de coleta, obtenção e transformação de dados, conectando o Power BI a um banco de dados MySQL hospedado no Microsoft Azure, construindo um modelo dimensional e um dashboard analítico.

🎯 Objetivo do Projeto
Provisionar um banco de dados Azure Database for MySQL
Modelar e popular tabelas de fato e dimensão (esquema estrela)
Conectar o Power BI ao MySQL na nuvem
Aplicar transformações de dados no Power Query (limpeza, tipos, colunas calculadas)
Criar um modelo de dados relacional dentro do Power BI
Escrever medidas DAX para as principais métricas do negócio
Construir um dashboard interativo com os insights obtidos
🧱 Arquitetura do Projeto
MySQL (Azure Database for MySQL)
        │
        │  Conector nativo MySQL
        ▼
   Power Query (ETL)
        │
        │  Transformações e limpeza
        ▼
   Modelo de Dados (Star Schema)
        │
        │  Medidas DAX
        ▼
   Dashboard Power BI (.pbix)
🗂️ Estrutura do Repositório
projeto-powerbi-mysql-azure/
├── README.md
├── sql/
│   ├── 01_create_database.sql       # Criação do banco e tabelas
│   ├── 02_insert_sample_data.sql    # Massa de dados de exemplo
│   └── 03_queries_analiticas.sql    # Consultas de apoio/validação
├── docs/
│   ├── modelo-dados.md              # Documentação do modelo (DER + esquema estrela)
│   ├── conexao-powerbi-mysql-azure.md  # Passo a passo de provisionamento e conexão
│   └── medidas-dax.md               # Medidas DAX documentadas
├── powerbi/
│   ├── instrucoes-montagem-pbix.md  # Roteiro para montar o .pbix no Power BI Desktop
│   └── dashboard.pbix               # (adicionar aqui após salvar no Power BI Desktop)
└── assets/
    └── (prints do dashboard finalizado)

⚠️ O arquivo .pbix é um formato binário proprietário do Power BI Desktop — por isso ele precisa ser salvo localmente na aplicação e depois adicionado a este repositório (veja powerbi/instrucoes-montagem-pbix.md).

🛠️ Tecnologias Utilizadas
Power BI Desktop
MySQL 8.0
Microsoft Azure – Azure Database for MySQL Flexible Server
Power Query (M)
DAX
🚀 Como Reproduzir
Provisione o banco no Azure e crie as tabelas — siga docs/conexao-powerbi-mysql-azure.md
Execute os scripts em sql/ na ordem (01, 02, 03)
Abra o Power BI Desktop e conecte ao MySQL — siga powerbi/instrucoes-montagem-pbix.md
Aplique as transformações do Power Query descritas em docs/modelo-dados.md
Cole as medidas de docs/medidas-dax.md
Monte as visualizações e salve o .pbix na pasta powerbi/
📈 Principais Indicadores do Dashboard
Receita total e ticket médio
Vendas por categoria de produto
Evolução de vendas ao longo do tempo
Top clientes e top produtos
Vendas por região/estado
🔗 Referências
Desafio original: DIO – Processando e Transformando Dados com Power BI
Documentação Power BI
Azure Database for MySQL
