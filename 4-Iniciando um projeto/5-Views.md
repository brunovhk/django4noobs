# 4.5 - Views

## O que são?

> Um model é a nossa descrição do dado que será gerenciado pela aplicação.
> Os models estão relacionados à estrutura do banco de dados. Neles contém os campos e comportamentos dos dados.

## Criando um View

Dentro da pasta template, crie um arquivo *HTML* com o nome do template definido anteriormente (**publicar.html**).
<p align="center">
<img src="../images/template.png">
</p>
Neste arquivo HTML iremos inserir o seguinte trecho de código:

```bash
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Django4Noobs - He4rt Developers</title>
</head>
<body>
    <h1>Olá mundo!</h1>
    <h2>Django4Noobs - He4rtDevelopers</h2>
</body>
</html>
```
Esta será nossa página HTML inicial .

Para defini-lá, iremos abrir o arquivo **views.py** do app **"blog4noobs"**.

Neste arquivo teremos o seguinte trecho de código:

```bash
from django.shortcuts import render

# Create your views here.
```
Como escrito no comentário, nele criaremos nossas Views. Iremos criar a View anteriormente já definida (**"publicar"**).

Utilize o trecho de código abaixo:

```bash
from django.shortcuts import render

def publicar(request):
    return render(request, "publicar.html")
```

## Vamos testar o que foi criado até agora!

No terminal de sua IDE, digite o comando abaixo:

```bash
python3 manage.py runserver
```

Se tudo ocorreu bem, você deverá ver uma mensagem como:

```bash
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.
```
Após isso, vá ao link indicado no terminal ou utilize o link no código acima e você deverá ter um resultado como na imagem abaixo:
<p align="center">
<img src="https://i.imgur.com/tcVGxCp.png">
</p>
