### Execução do Projeto - Ambiente de Desenvolvimento

Comandos para iniciar o ambiente de desenvolvimento:

Acessar a pasta raiz do projeto e executar o docker compose:
```
docker compose up -d
```

Após subir o ambiente docker, deve-se acessar o container da aplicação e executar os seguintes comandos:

Acessar o terminal do container de aplicação:
```
docker exec -it application bash
```

Ajustar permissões:
```
chown -R www-data:www-data ../www
chmod -R 777 ../www
```

Executar migrations do banco de dados:
```
php artisan migrate
```

Acessar a aplicação pelo navegador através do endereço abaixo:

[http://localhost:81](http://localhost:81)

### É possivel consultar as informações pelas rotas:
-http://127.0.0.1:8000/api/serviços

-http://127.0.0.1:8000/api/prestadores
