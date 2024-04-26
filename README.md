# lab-dio-cogn-search-2024
Atividade IA Azure MS | Cognitive Search

DIO Ia MS Bootcamp 2024 - Azure Cognitive Search
Atividade com Azure Cogn. Search.

# Leticia Ferreira

P.S.: Quase perdi a data limite mas corri para completar
❉ Inicialmente acessar e logar: https://portal.azure.com/#home

   ✰ Crie um novo repositório no github com um nome a sua preferência
                
                 Criei esse repositório em que está lendo meu READ.me, inclusive agradeço a atenção. Sou bem iniciante no GitHub por isso peço descupas por possíveis erros cometidos.
    Crie um um arquivo readme.md descrevendo o passo a passo para se configurar uma pesquisa, assim como seus insights, possibilidades de ferramentas que se beneficiam com esse tipo de ferramenta e aprendizados adquiridos durante o processo.

Passo a passo de como configurei uma pesquisa:

    1. Criar um novo recurso no Azure AI Search preenchendo as informações abaixo (deixei em inglês como exemplo):

     • Subscription: Your Azure subscription.
     • Resource group: Select or create a resource group with a unique name.
     • Service name: A unique name.
     • Location: Choose any available region.
     • Pricing tier: Basic

    Eu utilizei o mesmo recurso do Azure AI Service que já tinha criado anteriormente por isso não anexei imagem nesta etapa


    Obs.: Após preencher essas informações deve-se clicar em review + create e após de ver a mensagem de validado create novamente (pode demorar alguns minutos para criar)

    2. Criar um recurso de Azure AI Service

       Retornar à página inicial do Azure portal e selecionar + create a resoure e clicar em criar um Azure AI Service (ver exemplo em imagem abaixo)

       i![Cogn_Search__lab2](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/5c5c478e-f672-4cfc-bfbe-67deced21af1)

       
       ![Cogn_Search__lab3](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/5d540417-7498-4cde-86cd-171f4cfdb7dd)


    Obs.: Após preencher os dados continuar em review + create e após aguardar a validação bem sucedida clicar novamente em create (que também pode demorar alguns minutos). Verificar detalhes se estão corretos 

    3. Criar um storage account 

      • Criar recurso -> criar Storage account 
      • Preencher dados necessários como exemplifica a imagem abaixo:

      ![Cogn_Search__lab4](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/dd7a02d2-272d-44cd-9daa-d430bcc60dba)

      

    Após o preenchimento dos dados, segue-se como acima selecionando create e depois review após aguardar a validação clicar em detalhes e configuração no menu lateral esquerdo e mudar a configuração para Allow Blob anonymous access -> enable -> save

     ![Cogn_Search__lab7](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/1d16718f-f136-48fa-8e89-fe35d3f94290)


    4. Upload de documentos para o container

       No menu à esquerda selecionar containers e em seguida em + container (ver imagem abaixo):

       ![Cogn_Search__lab8](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/84ac0769-8403-4a13-85fc-f907e7e17bdb)


    • Preencher com os dados a seguir(nesse acabei não salvando imagem enquanto fazia mas no meu não tem o "-"): 
       Name: coffee-reviews
       Public access level: Container (anonymous read access for containers and blobs)
       Advanced: no changes.

     • Extrair arquivos do link a seguir (é seguro, pois trata-se de conteúdo oficial da MS): https://aka.ms/mslearn-coffee-reviews

       Selecionar container criado -> coffeereviews (no meu caso) e clicar em upload 
      ![Cogn_Search__lab10](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/8be0b3c1-ee89-4488-9155-3e00816d9a14)


       Obs.: Selecionar "Select a file" em Upload blob 


     5. Indexar documentos 

        Retornando à pagina Overview -> Data source -> Azure Blob Storage 

        Preencher dados abaixo (mais uma vez não adicionei iagem nesse):
       
        Data Source: Azure Blob Storage
        Data source name: coffee-customer-data
        Data to extract: Content and metadata
        Parsing mode: Default
        Connection string: *Select Choose an existing connection. Select your storage account, select the coffee-reviews container, and then click Select.
        Managed identity authentication: None
        Container name: this setting is auto-populated after you choose an existing connection.
        Blob folder: Leave this blank.
        Description: Reviews for Fourth Coffee shops.

        Obs.: Há + outros detalhes que precisam ser adicionados que vou adicionar no link de referências (precisam ser selecionados com cuidado e atenção)

         i![Cogn_Search__lab13](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/a34cc7b3-d6ca-4326-a24c-8e9a54195fc4)


        Esta etapa precisa ser detalhada e feita com cuidado porque é onde a conexão entre o container, indexer, skillsets etc. serão conectados para gerar os resultados 
       ![Cogn_Search__lab11](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/ff71218f-d99d-424d-bdac-3350e38e6c03)

         Ao selecionar um indexer é possível ver detalhes 

        ![Cogn_Search__lab14](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/55330980-feab-410d-903a-8012b1109ae8)
        

    6. Pesquisar 

       Overview -> Search Explorer

       Escolher opção de JSON view ao lado direito 

       As imagens a seguir mostram exemplos de pesquisa abaixo

       ![Cogn_Search__lab17](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/3d38a96c-5ba3-4648-9eef-bf9e3295d50e)


       ![Cogn_Search__lab18](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/a93ae590-bb47-450b-b973-f39cc6e02c47)



    7. Ver dados de imagens da knowledge Storage
     
        Ao abrir um documento é possível ver como ele é salvo para ser encontrado e identificado pela IA

       ![Cogn_Search__lab19](https://github.com/Leticia7/lab-dio-cogn-search-2024/assets/65042673/5900d462-bd6b-401a-8b5d-f152b386e058)

         

          
   ✰ Compartilhe conosco o link desse repositório através do botão 'entregar projeto' 
                
      Feito

❉ Links de Refência

    https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html
    https://aka.ms/mslearn-coffee-reviews
