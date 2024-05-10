Bom dia, aluno! Espero que esteja tudo tranquilo!

Analisei o seu código e identifiquei que a tabela não está sendo gerada no banco de dados. Sendo assim, sugiro as seguintes modificações para a execução correta dos containers:

Gere um diretório chamado database e crie seu script SQL dentro dele:

    use database;

    CREATE TABLE IF NOT EXISTS `people` (`id` int NOT NULL AUTO_INCREMENT, `name` varchar(255) NOT NULL, PRIMARY KEY(`id`));

Para que o container identifique onde está o script que deve ser executado ao iniciar, é necessário adicionar a seguinte linha em volumes no serviço do banco de dados:

    - ./database:/docker-entrypoint-initdb.d/

Faça as modificações e teste novamente a aplicação.

Sinta-se à vontade para perguntar sobre qualquer outra coisa!
Atenciosamente, Rafael.





