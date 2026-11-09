# 🎓 Portal de Simulados ENADE — Engenharia de Produção

Plataforma web interativa desenvolvida para apoiar a preparação dos estudantes do curso de **Engenharia de Produção** da **Universidade Federal do Ceará (Campus Russas)** para o **ENADE 2026**.

---

## 🚀 Link de Acesso Público

O acesso é gratuito, universal e funciona em qualquer navegador (computador, tablet ou celular) sem necessidade de instalação:

👉 **[Acessar o Portal de Simulados ENADE 2026](https://gepro1.github.io/simulado-enade-2026/)**

👉 **[Acessar a cartilha do ENADE 2026](https://github.com/marcelacostaaraujo21/enade-compass-2026.git).**

---

## 📖 Como Adicionar um Novo Simulado (`02.html`, `03.html`...)

Como o portal gera os botões dinamicamente via JavaScript, adicionar uma nova avaliação é muito simples e evita erros de formatação na página.

### Passo 1: Enviar o novo arquivo para o GitHub
1. No repositório, clique no botão **Add file** > **Upload files**.
2. Selecione o arquivo `.html` do novo simulado do seu computador.
3. Certifique-se de que o nome do arquivo seja curto e padronizado (exemplo: `02.html`).
4. Clique no botão verde **Commit changes**.

### Passo 2: Cadastrar o simulado no `index.html`
1. Abra o arquivo **`index.html`** no GitHub e clique no ícone de lápis ✏️ (**Edit file**).
2. Role até o final do arquivo, na seção dentro da tag `<script>`.
3. Localize a lista `listaSimulados` e adicione o bloco do novo simulado separado por uma vírgula `,`:

```javascript
// Adicione este bloco dentro da listaSimulados = [ ... ]:
{
    id: "02",
    arquivo: "02.html",
    titulo: "Simulado Módulo II — Qualidade & PCP",
    descricao: "15 Questões Objetivas",
    badge: "Novo",
    badgeCor: "bg-blue-500",
    destaque: false
}
