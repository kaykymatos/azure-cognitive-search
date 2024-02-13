## Criação de Recursos no Azure:
 - Faça login no portal do Azure.
 - Clique em "+ Criar um recurso", busque por "Azure AI Search" e crie um recurso Azure AI Search com as configurações necessárias, como nome do serviço único, localização, e tier básico.
 - Após a implantação, clique em "Ir para o recurso" para acessar a página de visão geral do Azure AI Search.

## Criação de Recurso Azure AI Services:
 - Na página inicial do portal Azure, clique em "+ Criar um recurso" e procure por "Azure AI Services".
 - Crie um plano de serviços Azure AI e, na página de configuração do recurso, configure o plano com as configurações necessárias, incluindo nome exclusivo e tier padrão.
 - Após a validação bem-sucedida, clique em "Criar".

## Criação de Conta de Armazenamento:
 - Novamente na página inicial do Azure, clique em "+ Criar um recurso" e procure por "Conta de Armazenamento".
 - Configure a conta de armazenamento com as configurações necessárias, como nome exclusivo, localização, desempenho padrão e redundância local.
 - Aguarde a implantação ser concluída.

## Configuração de Conta de Armazenamento:
 - Na conta de armazenamento criada, selecione "Configuração" no menu à esquerda.
 - Altere a configuração para permitir acesso anônimo a blobs para "Habilitado" e clique em "Salvar".

## Upload de Documentos para o Azure Storage:
 - No menu à esquerda, selecione "Containers" na conta de armazenamento.
 - Crie um novo contêiner chamado "coffee-reviews" com acesso público para leitura anônima.
 - Baixe e extraia os documentos de análises de café de https://aka.ms/mslearn-coffee-reviews para a pasta "reviews".
 - Faça upload desses arquivos para o contêiner "coffee-reviews".

## Indexação de Documentos com Azure AI Search:
 - No portal Azure, acesse o recurso Azure AI Search.
 - Na página de visão geral, selecione "Importar dados".
 - No assistente de importação de dados, escolha "Azure Blob Storage" como origem de dados e forneça os detalhes, incluindo a conexão com a conta de armazenamento e o contêiner "coffee- reviews".
 - Adicione habilidades cognitivas, configure um conjunto de habilidades chamado "coffee-skillset", habilite OCR e outras opções.
 - Salve as enriquecimentos em um repositório chamado "knowledge-store" na conta de armazenamento.

## Configuração do Índice e Indexador:
 - Personalize as configurações do índice, definindo o nome como "coffee-index" e configurando os campos padrão.
 - Crie um indexador chamado "coffee-indexer", agendando-o para executar uma vez com opções avançadas configuradas.
 - Submeta para criar o data source, conjunto de habilidades, índice e indexador.

## Monitoramento e Verificação:
 - Volte à página do recurso Azure AI Search.
 - Sob "Gestão de Pesquisa", selecione "Indexadores" e escolha o indexador recém-criado.
 - Aguarde até que o Status indique sucesso e revise os detalhes do indexador para garantir que foi criado com sucesso.

Esse processo cria um sistema de pesquisa alimentado por IA para analisar e extrair insights de análises de clientes armazenadas em documentos.
