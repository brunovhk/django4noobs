# 4.2 - Iniciando um projeto
Com o Django instalado, iremos iniciar nosso projeto.

No terminal da nossa IDE, utilizaremos o comando abaixo para iniciarmos um projeto:

```bash
django-admin startproject projeto4noobs
```

> Altere "projeto4noobs" pelo nome que deseja colocar em seu projeto.

Após esse comando nosso projeto será criado e teremos seguinte estrutura de pastas:

```bash
C:.
└───projeto4noobs
    │   manage.py
    │
    └───projeto4noobs
            asgi.py
            settings.py
            urls.py
            wsgi.py
            __init__.py
```

# Entendendo as pastas

Após criar o projeto, teremos duas pastas:

- Na primeira pasta teremos a raiz do projeto, contendo todos os arquivos do projeto;
- Na segunda pasta teremos os arquivos de configuração do projeto.

# Entendendo os arquivos

Criado nosso projeto, teremos alguns arquivos. Mas pra que servem cada um deles? Veja abaixo:

- <h3>init.py</h3>
    - O Python utiliza este arquivo para saber que a pasta é um módulo e dizer ao Django que há arquivos a serem
      executados.

- <h3>settings.py</h3>
    - Nosso arquivo principal de configuração do projeto. Aqui podemos encontrar os middlewares, diretório base,
      aplicativos do projeto e path dos arquivos estáticos.

- <h3>urls.py</h3>
    - Nosso arquivo principal de configuração de URLs da aplicação e do admin.

- <h3>wsgi.py</h3>
    - O Django utilizará o WSGI para hospedar qualquer aplicação Python que suporte a interface WSGI.

- <h3>manage.py</h3>
    - Este é o nosso arquivo principal, com ele poderemos controlar muitas coisas que acontecem no Framework.

### Conclusão:

**Nesta aula você aprendeu como criar um projeto como funcionam as pastas e arquivos, na próxima aulas aprenderemos como criar um módulo para nosso projeto**

**Bons estudos !!**

Ir para: [4.2 - Criando um módulo](3-Módulos.md)
