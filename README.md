# test_jukebox


## Instalação com docker 

 - #### CASO NÃO QUEIRA USAR DOCKER [Clique aqui](https://github.com/Wallacewss2033/test_jukebox/blob/main/README-A.md)

- Clone o projeto
```
git clone git@github.com:Wallacewss2033/test-jukebox.git
```
- Entre na raiz do prejeto ```test-jukebox``` e clone o projeto ```backend-jukebox```
```
git clone git@github.com:Wallacewss2033/backend-jukebox.git
```

### Back-end
- ainda na pasta raíz do projeto ```test-jukebox``` rode:
```
docker-compose up -d --build
```
- entre no terminal do container do projeto ```backend-jukebox``` 
 ```
 docker exec -it backend-jukebox bash
 ```
- no terminal do container rode:

```
composer install
```
- logo após rode esses comandos ```(fora do terminal do container)```
```
cp .env.example .env
```
```
php artisan key:generate
```

- Não esqueça de configurar o banco de dados na ``` .env ```
  
![image](https://github.com/Wallacewss2033/fullstack-challenge-20231205/assets/39920409/ec726dce-7762-4c68-b66c-668698afad41)

OBS: user e senha do mysql ambos são ```root```

- Volte para o terminal do container. Para criar o banco de dados e rode:
```
php artisan migrate
```

- Não esqueça de configurar o firebase

    Coloque o id do seu projeto firebase
    
    ![image](https://github.com/Wallacewss2033/test_jukebox/assets/39920409/846211a3-239b-4fcb-84cb-a5cc9f863c0d)



OBS: CASO HAJA ALGUM PROBLEMA DE PERMISSÃO NO PROJETO RODE:

```
chown -R root:www-data storage
```
```
chmod -R 777 ./storage
```
```
chmod -R 775 ./storage
```

    
# Frontend

Após rodar o comando de buildar os containers o frontend já estará pronto, apenas configure a .env 

![image](https://github.com/Wallacewss2033/test_jukebox/assets/39920409/0719bc2c-47bb-4672-932c-6d663d31d0e1)
