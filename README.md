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

| # | Desafio | Descrição | Como reproduzir | Issue |
|---|---------|-----------|-----------------|-------|
| 1 | Pirâmide de Palavras | Extensão `.pitugues` não detecta o dialeto automaticamente, contrariando a [wiki](https://github.com/DesignLiquido/delegua/wiki/Dialetos#dialetos-por-linha-de-comando) | `delegua arquivo.pitugues` falha, `delegua --dialeto pitugues arquivo.pitugues` funciona | [delegua-node#48](https://github.com/DesignLiquido/delegua-node/issues/48) |
| 2 | Pirâmide de Palavras | Hover do VS Code exibe sintaxe do Delégua (`var`) em vez da sintaxe do Pituguês | Passar o mouse sobre `imprima()` em arquivo `.pitugues` | [vscode#88](https://github.com/DesignLiquido/vscode/issues/88) |
| 3 | Pirâmide de Palavras | Extensão "Design Líquido - Linguagens em Português" do VS Code emite falso positivo "variável declarada mas nunca usada" para variáveis usadas dentro de `para cada` | Declarar variável no ambiente global e chamar dentro de um loop `para cada` | [delegua#1170](https://github.com/DesignLiquido/delegua/issues/1170) |
| 4 | Primeiro índice de um caractere | `retorna` dentro de `para cada` dentro de uma `funcao` não encerra a função, se comporta como `continue`, fazendo o loop continuar e o código após o loop também executar | Registrado no arquivo [desafios/primeiro_indice.pitugues](desafios/primeiro_indice.pitugues) | [delegua#1180](https://github.com/DesignLiquido/delegua/issues/1180) |
| 5 | Primeiro índice de um caractere | Operadores de atribuição compostos (`+=`, `-=`, etc.) funcionam mas não estão documentados na [wiki do Pituguês](https://github.com/DesignLiquido/pitugues-docs/wiki/Operadores) | Usar `indice += 1` em qualquer arquivo `.pitugues` funciona, mas a wiki não menciona | [pitugues-docs#5](https://github.com/DesignLiquido/pitugues-docs/issues/5) |

## Sugestões de features
 
Features existentes em Python que poderiam enriquecer o Pituguês, identificadas durante os desafios.
 
| # | Desafio | Descrição | Referência | Issue |
|---|---------|-----------|------------|-------|
| 1 | Primeiro índice de um caractere | Função equivalente ao `enumerate()` do Python para iterar com índice e valor ao mesmo tempo | [enumerate - Python docs](https://www.w3schools.com/python/ref_func_enumerate.asp) | [delegua#1181](https://github.com/DesignLiquido/delegua/issues/1181) |
| 2 | Primeiro índice de um caractere | Método de texto equivalente ao `str.find()` do Python para encontrar o índice da primeira ocorrência de um caractere | [find - Python docs](https://www.w3schools.com/python/ref_string_find.asp) | [delegua#1182](https://github.com/DesignLiquido/delegua/issues/1182) |
 
## Referências

- [Repositório original dos desafios](https://github.com/cumbucadev/desafios-pitugues)
- [Documentação do Pituguês](https://github.com/DesignLiquido/pitugues-docs/wiki)
- [Delégua no npm](https://www.npmjs.com/package/delegua)
- [Wiki de Dialetos do Delégua](https://github.com/DesignLiquido/delegua/wiki/Dialetos#pituguês)