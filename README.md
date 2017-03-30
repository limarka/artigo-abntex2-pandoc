# artigo-abntex2-pandoc

Modelo de artigo utilizando pandoc e abntex.

**OBS**: Esse repositório é EXTREMAMENTE EXPERIMENTAL. Em fase embrionária. No futuro, seu conteúdo irá ser incorporado a ferramenta limarka.

Chat para conversar sobre esse repositório: [https://gitter.im/abntex/limarka](https://gitter.im/abntex/limarka)

# Requerimentos

- ruby
- rake
- [guard](https://github.com/hawx/guard-shell)
- pandoc
- pandoc_abnt
- latex
- latexmk

# Compilação

Para geração do PDF execute:

    rake

Para apagar os arquivos gerados durante a compilação:

    rake clean

## Compilação automática

Quando você salvar as alterações no arquivo `artigo.md` ele será compilado automaticamente.

Para iniciar a compilação automática execute:

    guard
