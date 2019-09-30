# Como publicar uma aplicação Django no Heroku

## Configurando a aplicação
1- Adicionar django-heroku no requirements.txt
2- Adicionar gunicorn no requirements.txt
3- Criar o arquivo Procfile com o seguinte conteúdo:

```
web: gunicorn pastaprincipaldaaplicacao.wsgi --log-file -
```

4- Configurar o ALLOWED_HOSTS (localhost e URL de publicação)
5- Configurar o STATIC_ROOT:

```
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
```

6- Adicionar a configuração do Heroku no settings.py

```
import django_heroku

...

django_heroku.settings(locals())
```

## Configurando Heroku

1- Criar um app no painel do Heroku
2- Entrar na aba Deploy e conectar seu Github
3- Escolher o repositório da sua aplicação
4- Clicar no botão deploy


## Tutorial de exemplo
https://devcenter.heroku.com/articles/getting-started-with-python?singlepage=true
