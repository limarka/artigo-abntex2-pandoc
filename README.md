# artigo-abntex2-pandoc

Modelo de artigo utilizando pandoc e abntex.

**OBS**: Esse repositório é EXTREMAMENTE EXPERIMENTAL. Em fase embrionária. No futuro, seu conteúdo irá ser incorporado a ferramenta limarka.

Chat para conversar sobre esse repositório: [https://gitter.im/abntex/limarka](https://gitter.im/abntex/limarka)

# Requerimentos

## Requerimentos mínimos

- ruby
- rake
- [guard](https://github.com/hawx/guard-shell)
- pandoc
- pandoc_abnt
- latex
- latexmk

## Requerimentos adicionais

Para se valer da geração automática do pdf, também será necessário:

- guard
- guard-shell
- pdfgrep

## Instalação das dependências no OSX

O comando abaixo instalará as requerimentos supracitados (mínimos e adicionais).

**Observações**:

1. O `mactex` é consideravelmente grande (~ 3 GB), então seu download há de demorar um pouco.
2. Em algum momento a instalação poderá pedir sua senha.
3. Apesar de OSX já possuir `ruby` e `rake` instalado por padrão, são versões mais antigas. É necessário instalar uma versão mais nova (por exemplo, ruby 2.3), para a instalação do `guard` não dar erros.


```shell
brew tap caskroom/cask && brew install pdfgrep pandoc ruby@2.3 && brew cask install mactex && sudo gem install pandoc_abnt guard guard-shell
```

# Compilação

Para geração do PDF execute:

    rake

Para apagar os arquivos gerados durante a compilação:

    rake clean

## Compilação automática

Quando você salvar as alterações no arquivo `artigo.md` ele será compilado automaticamente.

Para iniciar a compilação automática execute:

    guard
