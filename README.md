Claro! Aqui está um `README.md` completo, ampliado e detalhado sobre a linguagem **TypeYts** — totalmente focado na linguagem em si, explicando todas as palavras-chave, estruturas, tipos e lógica de uso. Ideal para incluir no repositório oficial:

```markdown
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
  ```

- `last` → ``Define o retorno de uma função declarada com flag.``  
  Exemplo: `last "texto"`

- `case` → ``Permite verificar múltiplos valores e executar ações para cada um.``  
  Exemplo:
  ```ty
  case comando {
    "ping": send("pong");
    "help": send("Ajuda!");
    default: send("Inválido");
  }
  ```

- `onStartup()` → ``Executa um bloco assim que o script inicia.``  
  Exemplo:
  ```ty
  onStartup() {
    log("Sistema iniciado.");
  }
  ```

- `onSlash("comando")` → ``Executa ao receber um comando do tipo /comando.``  
  Exemplo:
  ```ty
  onSlash("ping") {
    send("🏓 Pong!");
  }
  ```

- `send()` → ``Envia mensagens, respostas de texto ou objetos (como embeds).``

- `log()` → ``Mostra uma saída no console, usado para debug ou registros.``

- `fileExists()` → ``Verifica se um arquivo existe antes de usá-lo.``  
  Exemplo:
  ```ty
  if (fileExists("data.json")) {
    log("Arquivo detectado.");
  }
  ```

---

## 🔠 Tipos de dados suportados

- **String**: textos entre aspas (`"Olá"` ou `'Mundo'`)
- **Número**: `1`, `0.5`, `-3`
- **Boolean**: `true`, `false`
- **Null**: valor nulo representado por `null`
- **Objeto**: estruturas de chave e valor, como:
  ```ty
  pers embed = {
    title: "Título",
    description: "Corpo da mensagem",
    color: "#00ffff"
  };
  send(embed);
  ```
- **Array**: suporte em desenvolvimento (ex: `["a", "b", "c"]`)

---

## 🔣 Operadores disponíveis

- **Aritméticos**: `+`, `-`, `*`, `/`, `%`
- **Comparação**: `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Lógicos**: `&&` (e), `||` (ou), `!` (negação)
- **Concatenação**: `+` (para unir strings ou valores)

---

## 💬 Fluxos e condições

O `case` funciona como um verificador múltiplo:

```ty
case comando {
  "start": send("Iniciado");
  "stop": send("Parado");
  default: send("Comando inválido");
}
```

Você também pode usar expressões lógicas combinadas com `get`:

```ty
get ativo = true;

if (ativo && fileExists("log.txt")) {
  log("Sistema pronto.");
}
```

---

## 🔁 Funções personalizadas

Com `flag`, você pode criar funções:

```ty
flag dobro(valor) {
  last valor * 2;
}
send("Resultado: " + dobro(5));
```

Funções podem receber parâmetros e retornar valores com `last`.

---

## 📤 Exemplos completos

```ty
pers prefix = "ty,";

onStartup() {
  log("Sistema iniciado com prefixo: " + prefix);
}

onSlash("ping") {
  send("🏓 Pong!");
}

flag somar(a, b) {
  last a + b;
}

case comando {
  "soma": send("Resultado: " + somar(4, 5));
  default: send("Nenhuma ação para este comando.");
}
```

---

## 📌 Observações

- Não é necessário ponto e vírgula no final das linhas
- Os nomes são sensíveis: `flag`, `Flag` e `FLAG` são diferentes
- Tudo é processado de forma sequencial
- Objetos são compatíveis com `send()` para construir respostas

---

## 👤 Autor

Desenvolvido por **RaihNoDev**  
Uma linguagem para quem busca clareza, simplicidade e controle.

```


