# 🐍 Meus Desafios em Pituguês

Repositório com minhas soluções para os [desafios de Pituguês](https://github.com/cumbucadev/desafios-pitugues/issues) propostos pela [cumbucadev](https://github.com/cumbucadev), com o objetivo de explorar e encontrar bugs na linguagem.

## Como rodar

### 1. Instale o Delégua

O Pituguês roda sobre o Delégua. Você precisa do [Node.js](https://nodejs.org) instalado e então:

```bash
npm install -g delegua
```

### 2. Execute um desafio

Há duas formas de rodar um arquivo `.pitugues`:

**Pela extensão do arquivo** (o Delégua detecta o dialeto automaticamente):

```bash
delegua desafios/piramide_de_palavras.pitugues
```

**Especificando o dialeto explicitamente:**

```bash
delegua --dialeto pitugues desafios/piramide_de_palavras.pitugues
```

### 3. Modo interativo (REPL)

Para explorar a linguagem no terminal sem precisar de um arquivo:

```bash
delegua --dialeto pitugues
```

## Bugs encontrados

Bugs e comportamentos inesperados encontrados durante os desafios serão documentados aqui.

| # | Desafio | Descrição | Como reproduzir |
|---|---------|-----------|-----------------|
| 1 | Pirâmide de Palavras | Extensão `.pitugues` não detecta o dialeto automaticamente, contrariando a [wiki](https://github.com/DesignLiquido/delegua/wiki/Dialetos#dialetos-por-linha-de-comando) | `delegua arquivo.pitugues` falha, `delegua --dialeto pitugues arquivo.pitugues` funciona |
| 2 | Pirâmide de Palavras | Hover do VS Code exibe sintaxe do Delégua (`var`) em vez da sintaxe do Pituguês | Passar o mouse sobre `imprima()` em arquivo `.pitugues` |
| 3 | Pirâmide de Palavras | Extensão "Design Líquido - Linguagens em Português" do VS Code emite falso positivo "variável declarada mas nunca usada" para variáveis usadas dentro de `para cada` | Declarar variável no ambiente global e chamar dentro de um loop `para cada` |


## Referências

- [Repositório original dos desafios](https://github.com/cumbucadev/desafios-pitugues)
- [Documentação do Pituguês](https://github.com/DesignLiquido/pitugues-docs/wiki)
- [Delégua no npm](https://www.npmjs.com/package/delegua)
- [Wiki de Dialetos do Delégua](https://github.com/DesignLiquido/delegua/wiki/Dialetos#pituguês)