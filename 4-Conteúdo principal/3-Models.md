# 4.3 - Models

## O que são?

> Um model é a nossa descrição do dado que será gerenciado pela aplicação.
> Os models estão relacionados à estrutura do banco de dados. Neles contém os campos e comportamentos dos dados.

## Criando um model

- Abra o arquivo **models.py** do seu app (**blog4noobs**) e teremos o trecho de código abaixo:

```bash
from django.db import models

# Create your models here.
```

Como diz o comentário, podemos criar nossas models nesse arquivo. Então vamos criar com o trecho de código abaixo:

```bash
from django.db import models

# Declaramos um novo modelo com o nome "BlogModel"
class BlogModel(models.Model):
    # Campos do nosso modelo
    titulo = models.CharField(max_length=200)
    conteudo = models.TextField()
    # Renomeia as instâncias do modelo com o título
    def __str__(self):
        return self.titulo
```

Após definirmos a estrutura do nosso banco de dados, vamos utilizar dois comandos para criar o banco de dados.
Primeiro, utilize o comando abaixo:

```bash
Python manage.py makemigrations
```

> O comando *makemigrations* analisa se foi feito alterações nos modelos. Se sim, ela cria novas *migrations* para
> alterar a estrutura do banco de dados.

Utilize o segundo comando:

```bash
Python manage.py migrate
```

> Após o comando *makemigrations* analisar e criar o banco de dados, o comando *migrate* executa e aplica as alterações.

Deveremos ter uma saída como:

```bash
python manage.py migrate

Operations to perform:
  Apply all migrations: admin, auth, blog4noobs, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying admin.0003_logentry_add_action_flag_choices... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying auth.0010_alter_group_name_max_length... OK
  Applying auth.0011_update_proxy_permissions... OK
  Applying auth.0012_alter_user_first_name_max_length... OK
  Applying blog4noobs.0001_initial... OK
  Applying sessions.0001_initial... OK
```

Temos nossas tabelas criadas. Vamos consultá-la utilizando o SQLite com os dois comandos abaixo:

```bash
$ sqlite3
$ .tables
```

Devemos ter a seguinte saída:

```bash
sqlite> .tables
auth_group                  blog4noobs_blogmodel
auth_group_permissions      django_admin_log
auth_permission             django_content_type
auth_user                   django_migrations
auth_user_groups            django_session
auth_user_user_permissions
```

Isso significa que nossas tabelas se encontram no banco de dados e podemos consultá-las.

### Conclusão:

**Nesta aula você aprendeu como criar um model e o que são models, na próxima aula aprenderemos como criar um template**

**Bons estudos !!**

Ir para: [4.4 - Templates](4-Templates.md)