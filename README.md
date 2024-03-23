# Laboratório AI-900

## Laboratório prático do Bootcamp Microsoft Azure

### Passos Iniciais

1. Primeiramente, é necessário criar uma conta no **Microsoft Azure** [aqui](https://azure.microsoft.com/pt-br/) (clique em "Experimentar gratuitamente"). Será necessário adicionar um cartão de crédito para fins de reconhecimento. No meu caso, foi cobrado R$5,00, que posteriormente foi reembolsado.

2. No site do Azure, clique em "Criar novo recurso" e em seguida em "Machine Learning" ou pesquise por "Machine Learning" no *marketplace*. Selecione **Azure Machine Learning** e clique em "Criar".

3. No campo "Assinatura", abaixo há a janela "Grupo de Recursos". Eu preenchi com **LABAI-900**. Esse item é semelhante a um armário com várias seções para organizar as roupas; no nosso caso, é o nosso projeto.

4. No próximo item, "Detalhes da nossa Área de Trabalho", no campo "Nome", que deve ser exclusivo, coloquei: **laboratorioai900**, tudo junto.

5. No campo "Região", escolhi: **East US**, pois o serviço é mais caro no Brasil. 😄

6. Os demais itens não devem ser alterados para este laboratório.

7. Depois, basta clicar em "Revisar e Criar" e aguardar até que o processo seja concluído. Em seguida, clique em "Criar" e aguarde o término do *deploy*.

8. Ao finalizar o processo, clique em "Ir para o recurso". Você será redirecionado para o site: [ml.azure.com](https://ml.azure.com).

9. Em alguns casos, será necessário fazer login. No meu caso, não foi necessário. Se for o caso, utilize as credenciais utilizadas para abrir a sua conta.

10. Neste site, devemos realizar as configurações iniciais. Este [link](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/02-content-safety.html) ajuda em caso de dúvidas maiores.

11. Clique em "Criar uma Área de Trabalho" e confirme algumas informações.

12. Na barra da esquerda, procure e clique em **ML Automatizado**.

### Configuração do ML Automatizado

13. Será descrito aqui os detalhes, mas é só seguir este [link da documentação](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html) para criar seu primeiro modelo de *Machine Learning*.

14. Clique em "Novo Trabalho de ML Automatizado".

15. Nos campos "Nome do Trabalho" e "Novo Nome do Experimento", foi sugerido inserir: **mslearn-bike-automl**; eu deixei o padrão.

16. Na descrição do projeto, inseri: **Aprendizado de Máquinas Automatizado para Previsão de Aluguéis de Bicicletas**.

17. Nos marcadores, deixe como "Nenhum" e avance para a próxima tela.

18. Selecione o tipo de tarefa como **Regressão** (tipo de algoritmo para treinar nosso projeto).

19. Clique em "Selecionar Dados" e, em seguida, em "Criar".

20. Defina o nome e o tipo de dados como **alugueisdebicicletas**, com a descrição "Dados históricos de aluguéis de bicicletas" e tipo "Tabular", e clique em "Avançar".

21. Selecione "Fontes de Dados de Arquivos da Web".

22. Insira a URL da documentação: [https://aka.ms/bike-rentals](https://aka.ms/bike-rentals) e clique em "Avançar".

23. Nas configurações, altere apenas o seguinte item: "Cabeçalhos de Colunas", altere para: **Somente o Primeiro Arquivo Tem Cabeçalhos**, e depois clique em "Avançar".

24. Em "Esquema", clique em "Avançar".

25. Em "Examinar", clique em "Avançar".

26. Clique no item criado, neste caso: **Aluguel de Bicicletas**, e depois em "Avançar".

### Configuração de Tarefas

27. **Coluna de Destino:** rentals (integer).

    27.1. Clique em "Definições de Configurações Adicionais" e deixe tudo desmarcado.
    
    27.1.1. Clique em "Modelos Permitidos" e selecione os itens: **RandomForest** e **LightGBM**.

28. Em "Limites", preencha da seguinte maneira:
    - Máximo de Avaliações: 3
    - Máximo de Avaliações Simultâneas: 3
    - Máximo de Nós: 3
    - Limites de Pontuação de Métricas: 0.085
    - Tempo Limite de Experimentos: 15 (minutos)
    - Tempo Limite de Interações: 15 (minutos)
    - Habilite a opção: Encerramento Antecipado.

29. No item "Validar e Testar", selecione o subitem "Tipo de Validação" e escolha a opção: **Divisão de Validação de Treinamentos** e em seguida clique em "Avançar".

30. Em "Computação", clique em "Avançar".

31. Em "Examinar", clique em "Enviar Trabalho de Treinamento" e aguarde.

32. Em seguida, procure a aba "Ponto de Extremidade" e clique em "Testar" para visualizar alguns resultados em .json.

33. Para exportar os dados em .json, clique na aba "Automação", em seguida em "Exportar Modelo" e depois em "Baixar". O arquivo estará zipado com o código e um template em .json.







