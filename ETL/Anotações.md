## ETL (extract, transformation, load)

Tipo de data integration em três etadas, usado para combinar dados de diversas fontes. Utilizado para construir um Data Warehouse.
Extrair: 
- import dos dados em vários formatos
- criação de pastas de trabalho

Transformar:
- colunas, linhas
- tipos de dados
- mesclar, acrescentar
- listas, tabelas

Load:
- carregar para o modelo de dados

## ETAPAS PARA ETL
1) Extract
   Consiste em se comunicar com outros sistemas ou outros BDs para capturar as informações que serão inseridas no destino.
   JSON, txt
2) Transformation
   Padronização, limpeza, qualidade.
   Pode ter vários padrões diferentes de nomenclatura ou tipo de dados.
3) Load
   Etapa final onde dados são lidos das áreas de Staging e preparação de dados.

Vantagens da ETL
- Garantia significativa da qualidade dos dados devido ao pré-processamento.
- Funcionalidade de execução (já possui funções específicas, exigindo atenção no fluxo de dados).
- Desenvolvimento das cargas (possibilidade de desenvolvimento de uma rotina de carga em uma ferramenta).
- Manutenção das cargas (tarefas têm rotina, facilitando a manutenção).
- Metainformação (informações úteis para identificar, localizar, entender e gerenciar dados).
- Performance (grandes volumes de dados com maior velocidade e recursos).
- Transferência (ferramentas de ETL podem ser deslocadas de um servidor para outro).
- Conectividade (múltiplas fontes de dados com conexões transparentes; facilidade de conexão com mais fontes caso necessário).
- Reinicialização das cargas (possível reiniciar o Extract e Load das cargas de onde pararam)
- Segurança e Estabilidade (possibilidade de articular a segurança, modulando e dividindo as finalidades).

## Ferramentas aplicadas para ETL
Softwares utilizados para facilitar o processo de interação de dados, utilizados em Data Warehouses, Data Marts e Business Intelligence.
Também utilizados em processos de integração de software, bancos de dados, etc.

  - IBM Data Stage
  - Power Center
  - Sql Server Integration Services
  - Talend ETL

Ferramentas ETL para Big Data (baseadas no ecossistema Hadoop)
  - SQOOP
  - HIVE
  - PIG
  - SPARK

## Biblioteca Pandas (Python)
  manipulação de dados estruturada de forma semelhante ao Excel.
1) Estrutura de dados
   - Series (matriz unidimensional composta por uma sequência de valores com indexação).
   - DataFrames (estrutura tabular, com linhas e colunas rotuladas).

## Scikit-learn library
  Permite realizar análises matemáticas e estatísticas.
  Pode criar um modelo de análise de modelos.
  Faz previsão do modelo ML criado.
## Matplotlib
  Realiza a exibição de gráficos e análises.

## Framework Luigi
  Framework criado pelo Spotify que cria pipelines de dados em Python. Lida com resolução de dependências, gerenciamento de fluxo de trabalho, visualização, tratamento de falhas, integração de linha de comando e mais.
  - Target: um alvo contém a saída de uma tarefa que pode ser um arquivo, uma relação com BD.
  - Tarefas: onde o trabalho ocorre. Pode ser dependente ou independente. Representada como uma classe com funções membro obrigatórias.

