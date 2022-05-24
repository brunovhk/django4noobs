## 2.3 - Ambiente Linux

### Passo a passo - Python3

Nosso ambiente de desenvolvimento nas distribuições Linux será bem simples de se instalar.

Vamos instalar o Python com alguns módulos para ajudar no desenvolvimento posteriormente.
Iremos instalar o Python e o gerenciador de pacotes "pip", utilizaremos ele nas próximas aulas.

Pra instalar tudo de uma vez, basta rodar o comando abaixo:

- Debian, Ubuntu e distribuições derivadas (apt):

```bash
sudo apt-get install python3-pip
```

- RedHat, CentOS e distribuições derivadas (yum):

```bash
sudo yum install python3-pip
```

Após a instalação, iremos verificar se tudo foi instalado corretamente com o comando abaixo:

```bash
which python
```

ou

```bash
which python3
```

Após rodar o comando, deverá retornar algo como:

```bash
/usr/bin/python
```

Isso significará que a instalação foi bem sucedida.

Caso sua distribuição não seja baseada no Debian (apt) ou RedHat (yum) você deve usar o gerenciador de pacotes apropriado para a sua
distribuição (pacman, zypper, ...).

Após finalizar com sucesso a instalação do Python e dos módulos, você pode conferir a versão instalada rodando o comando
abaixo:

```bash
python --version
```

O retorno do comando acima deve exibir algo parecido com:

```bash
Python 3.10.4
```

### Passo a passo - SQLite:
* Basta digitar o comando abaixo para instalar o SQLite3:

```bash
sudo apt install sqlite3
```

Você pode verificar a versão do SQLite digitando o comando abaixo:

```bash
sqlite3 –version
```

Ir para: [2.4 Ambiente MacOS](4-Ambiente-macos.md)
