# ⚙️ TypeYts

**TypeYts** é uma linguagem de script desenvolvida por **RaihNoDev**, criada com o objetivo de proporcionar uma sintaxe simples, legível e altamente funcional para automações, bots e fluxos lógicos. Com comandos diretos e comportamento previsível, TypeYts elimina a complexidade excessiva de outras linguagens, focando na expressividade do que você quer que o código faça.

A linguagem usa arquivos com extensão `.ty`, e todo o seu código é baseado em palavras-chave específicas, sem necessidade de ponto e vírgula, tipos rígidos ou blocos verbosos. Seu foco está na escrita fluida, onde cada linha representa uma instrução clara e objetiva.

---

## 📚 Palavras-chave e descrição

- `pers` → ``Declara uma constante imutável.``  
  Exemplo: `pers prefix = "ty,"`

- `get` → ``Declara uma variável mutável que pode ser reatribuída.``  
  Exemplo: `get contador = 0`

- `flag` → ``Cria uma função personalizada com parâmetros.``  
  Exemplo:
  ```ty
  flag somar(a, b) {
    last a + b;
  }
