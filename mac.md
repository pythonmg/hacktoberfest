# Installacao do *Git* no *MacOS*

[Abra uma janela do terminal.](https://www.youtube.com/watch?v=okzqund_EbQ)

## Primeiro passo – Instalar o [*Homebrew*](http://brew.sh/)

> *Homebrew* é um sistema de gerenciamento de pacotes de software livre e de código aberto que simplifica a instalação do software no sistema operacional macOS da Apple e no Linux .

**Copie e cole o seguinte** na janela do terminal e **pressione `Enter`**.

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
Brew Doctor é a ferramenta de auto-diagnóstico da Homebrew
```
brew doctor
```

Você será solicitado a instalar as *Ferramentas de Desenvolvedor de Linha de Comando* da *Apple*. **Confirme clicando em *Instalar***. Após a conclusão da instalação, continue instalando o *Homebrew* by **pressionando `Enter`** novamente.

## Segundo passo – Instalar o *Git*

**Copie e cole o seguinte** na janela do terminal e **pressione `Enter`**.

```shell
brew install git
```

**Você pode começar a usar o *Git*.**
