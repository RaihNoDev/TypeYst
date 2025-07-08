<div align="center">
  <img src="https://media.discordapp.net/attachments/1391612190892490845/1392259142625918976/ty-icon.png" height="128" />

  <h1>⚙️ TypeYts</h1>
  <p><strong>Linguagem de script feita pra bots com alma hacker.</strong></p>
  <p><em>🛠️ Criada por <strong>RaihNoDev</strong></em></p>

  <img src="https://img.shields.io/badge/sintaxe-minimalista-00ffff?style=for-the-badge&logo=terminal&logoColor=00ffff" />
  <img src="https://img.shields.io/badge/estilo-terminal--hacker-green?style=for-the-badge" />
</div>

---

## 🚀 O que é a TypeYts?

TypeYts é uma linguagem baseada em comandos simples que você escreve como se estivesse num terminal. Ela é feita pra facilitar a criação de bots, fluxos e funções automatizadas, com uma sintaxe limpa, sem ponto e vírgula obrigatório e com foco em **clareza + velocidade**.

Não é JavaScript. Não é YAML. É TypeYts.

---

## ✨ Como funciona

Em TypeYts, você cria comandos com palavras-chave diretas como `pers`, `get`, `flag`, `case`, `send()` e `onStartup()`. A lógica flui como um script de terminal.

Exemplo:

```ty
pers prefix = "ty,";

onStartup() {
  log("Bot iniciado com prefixo: " + prefix);
}

onSlash("ping") {
  send("🏓 Pong!");
}
