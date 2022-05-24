# 4.5 - Configurando as URLs

Com o projeto e app criados, podemos agora partir para a configuração do projeto.

### Nota:

> Para cada app que criamos, teremos que registrá-lo nas configurações.

Então iremos abrir o arquivo para configurar, o arquivo será o **settings.py**

No projeto que criamos anteriormente, o caminho será:

> projeto4noobs/projeto4noobs/settings.py

Iremos adicionar a constante do nosso app na no trecho **INSTALLED_APPS** dentro do arquivo **settings.py** para que o
módulo
seja registrado.

O nome app que definimos anteriormente é "blog4noobs", então deverá ficar assim:

```bash
# Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'blog4noobs',
]
```

Após isso, teremos que criar um arquivo **"urls.py"** dentro da pasta blog4noobs. A estrutura de pastas deverá ficar
assim:

```bash
C:.
│   manage.py
│
├───blog4noobs
│   │   admin.py
│   │   apps.py
│   │   models.py
│   │   tests.py
│   │   urls.py
│   │   views.py
│   │   __init__.py
│   │
│   ├───migrations
│   │       __init__.py
│   │
│   └───templates
│           publicar.html
│
└───projeto4noobs
        asgi.py
        settings.py
        urls.py
        wsgi.py
        __init__.py
```

Iremos abrir este arquivo para configurar as urls do nosso app "blog4noobs".

Dentro deste arquivo, iremos configurar com o seguinte trecho de código:

```bash
from django.urls import path
from . import views

urlpatterns = [
    path('', views.publicar, name='publicar'),
]
```

Note que no trecho de código estamos importando todas as views, e referenciando uma view chamada **"publicar"**, porém
não temos ela ainda e iremos criar
posteriormente.

Agora temos que configurar no arquivo de URLs principal.

No projeto que criamos anteriormente, o caminho será:

> projeto4noobs/projeto4noobs/urls.py

O código estará assim:

```bash
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]
```

Então iremos importar o **include** do **django.urls** e referenciar a url em **urlspatterns**.

Nosso resultado será o seguinte:

```bash
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('', include('blog4noobs.urls')),
    path('admin/', admin.site.urls),
]
]
```

### Nota:

> - **path:** Este método é responsável por criar as urls, ele recebe parâmetros como o próprio path e a view ou o
    conjunto de views que serão acessadas;
> - **include:** Este método serve para que possamos incluir um conjunto de views.

Este arquivo é muito importante, e representa todas as URLs do nosso projeto. Todas as URLs que criamos no app "
blog4noobs" serão importadas a partir da linha:

```bash
path('', include('blog4noobs.urls')),
```

### Conclusão:

**Nesta aula você aprendeu como criar as URLs do nosso projeto, na próxima aula aprenderemos como criar
nossas views.**

**Bons estudos !!**

Ir para: [4.6 - Views](6-Views.md)
