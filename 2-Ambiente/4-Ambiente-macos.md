## 2.4 - Ambiente MacOS

Para o ambiente MacOS é preciso fazer a instalação do XCode, que pode ser baixado
na <a href='https://apps.apple.com/br/app/xcode/id497799835'>App Store</a>, do pacote para desenvolvimento em linha de
comando no macOS, command line tools e dos gerenciadores de pacotes pip e homebrew.

## 2.4.1 - Passo a passo:

- Para instalar o *command line tools*, basta rodar o comando abaixo:

  ```bash
  $ xcode-select --install
  ```

- Para instalar o *pip*, basta rodar o comando abaixo:

  ```bash
  $ sudo easy_install pip
  ```

- Iremos atualizar o *pip*. Para isso, basta rodar o comando abaixo:

  ```bash
  $ sudo pip install --upgrade pip
  ```

- Para instalar o *HomeBrew*, rode o comando abaixo:

  ```bash
  $ ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
  ```

- E finalmente instalaremos o *Python 3*:

  ```bash
  $ brew install python3
  ```

Para mais informações sobre como instalar o PHP utilizando homebrew no MacOS:

https://python.org.br/instalacao-mac/

Ir para: [3 - Como Funciona o Django?](../3-Entendendo%20a%20estrutura/00-Ciclo.md)
