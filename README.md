# compose-n8n
Neste exemplo, estamos usando o serviço postgres para fornecer um banco de dados PostgreSQL para o serviço n8n. O serviço postgres é definido usando a imagem oficial do PostgreSQL.

Na seção environment do serviço n8n, estamos definindo as variáveis de ambiente necessárias para se conectar ao banco de dados PostgreSQL. Estamos usando o driver postgresdb e definindo o nome do banco de dados, o host, a porta, o usuário e a senha.

Também estamos definindo uma dependência entre os serviços n8n e postgres para garantir que o banco de dados esteja em execução antes que o serviço n8n tente se conectar.

Por fim, estamos montando o volume ~/.n8n para o serviço n8n e o volume postgres-data para o serviço postgres, que é usado para persistir os dados do banco de dados.

Você pode salvar este arquivo em um diretório no seu servidor e iniciar o serviço usando o comando docker-compose up -d. Certifique-se de ter o Docker e o Docker Compose instalados em seu servidor antes de executar este comando.
