# ⚙️ TypeYts

**TypeYts** é uma linguagem de script criada por **RaihNoDev**, feita para lógica clara, escrita simples e uso em automação de fluxos ou bots. Seu foco é a simplicidade: arquivos `.ty` são escritos com palavras-chave diretas que descrevem ações e comportamentos do sistema de forma legível e direta.

---

## ✨ Visão geral

- Sintaxe limpa e sem necessidade de ponto e vírgula
- Palavras-chave autoexplicativas
- Suporte nativo a funções, condições, eventos e objetos
- Arquivos `.ty` direto ao ponto

---

## 📚 Palavras-chave e estruturas

- `pers` → ``Constante imutável``
- `get` → ``Variável mutável``
- `flag` → ``Declaração de função personalizada``
- `last` → ``Valor de retorno de uma função``
- `case` → ``Estrutura condicional com múltiplas opções``
- `onStartup()` → ``Executado quando o script inicia``
- `onSlash("comando")` → ``Dispara ao receber um comando de barra``
- `send()` → ``Envia mensagens, texto ou objetos``
- `log()` → ``Exibe mensagens no terminal (debug)``
- `fileExists()` → ``Verifica se um arquivo existe no sistema``

---

## 📦 Tipos de dados

- Strings: `"texto"`
- Números: `10`, `-3.5`
- Booleanos: `true`, `false`
- Null: `null`
- Objetos: `{ chave: valor }`
- Arrays: `["item1", "item2"]` *(em desenvolvimento)*

---

## 🔣 Operadores

- Aritméticos: `+`, `-`, `*`, `/`, `%`
- Comparação: `==`, `!=`, `>`, `<`, `>=`, `<=`
- Lógicos: `&&`, `||`, `!`
- Concatenação: `+` para strings

---

## 🧠 Exemplo

```ty
pers prefix = "ty,";

onStartup() {
  log("Prefixo definido: " + prefix);
}

onSlash("ping") {
  send("🏓 Pong!");
}

flag somar(a, b) {
  last a + b;
}

case comando {
  "oi": send("Olá!");
  "soma": send("2 + 3 = " + somar(2, 3));
}
