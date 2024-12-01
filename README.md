# Análise de Documentos Anti-fraude com AzureAI

Este projeto oferece uma solução para realizar a análise de documentos de cartões de crédito utilizando a tecnologia AzureAI. Desenvolvido em **Python**, a aplicação utiliza **Streamlit** para criar uma interface simples onde o usuário pode fazer o upload de imagens de documentos e validar as informações do cartão de crédito, como o nome do titular, banco emissor e data de validade. O sistema armazena as imagens enviadas no **Azure Blob Storage** e realiza a análise do documento com o **Azure AI** para identificar a validade do cartão de crédito.

## Funcionalidades:

1. **Upload de Imagens**: O usuário pode carregar imagens de arquivos de formato PNG, JPG ou JPEG.
2. **Armazenamento no Azure Blob Storage**: Após o upload, o arquivo é enviado para o Azure Blob Storage, onde é armazenado de forma segura.
3. **Análise Anti-fraude**: Utiliza o serviço Azure AI para analisar o conteúdo da imagem do cartão de crédito e verificar se ele é válido, mostrando as informações como:
   - Nome do titular
   - Banco emissor
   - Data de validade do cartão
4. **Resultado da Validação**: O resultado da análise é exibido na interface, informando se o cartão de crédito é válido ou não, com detalhes sobre o cartão.

## Como Usar:

1. **Instalar as Dependências**:
   Para instalar as dependências necessárias, execute o seguinte comando:

   ```bash
   pip install -r requirements.txt
   ```

2. **Configurar o Arquivo `.env`**:
   Preencha as variáveis no arquivo `.env` com as credenciais e configurações do Azure:

   ```env
   ENDPOINT = ""
   SUBSCRIPTION_KEY = ""
   AZURE_STORAGE_CONNECTION_STRING = ""
   CONTAINER_NAME = "Cartoes"
   ```

   - **ENDPOINT**: O endpoint da sua conta Azure Cognitive Services.
   - **SUBSCRIPTION_KEY**: A chave de assinatura para autenticação no Azure Cognitive Services.
   - **AZURE_STORAGE_CONNECTION_STRING**: A string de conexão para o Azure Blob Storage.
   - **CONTAINER_NAME**: O nome do container no Azure Blob Storage onde as imagens serão armazenadas.

3. **Iniciar o Streamlit**:
   Para iniciar a aplicação Streamlit, execute o seguinte comando:

   ```bash
   streamlit run .\app.py
   ```

   Isso abrirá a interface no seu navegador, permitindo que você faça o upload de arquivos de imagem e visualize os resultados da análise.

## Tecnologias Utilizadas:

- **Python**: Linguagem de programação principal utilizada no projeto.
- **Streamlit**: Para criação da interface interativa.
- **Azure Blob Storage**: Para armazenamento seguro das imagens enviadas.
- **Azure AI**: Para realizar a validação e extração de informações dos documentos de cartão de crédito.

Este projeto tem como objetivo ajudar na prevenção de fraudes em processos que envolvem documentos e cartões de crédito.
