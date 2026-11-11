# 🎓 Portal de Simulados ENADE — Engenharia de Produção

Plataforma web interativa desenvolvida para apoiar a preparação dos estudantes do curso de **Engenharia de Produção** da **Universidade Federal do Ceará (Campus Russas)** para o **ENADE 2026**.

---

## 🚀 Link de Acesso Público

👉 **[Acessar o Portal de Simulados ENADE 2026](https://gepro1.github.io/simulado-enade-2026/)**

👉 **[Acessar o aplicativo e a cartilha do ENADE 2026](https://enade-compass-2026.lovable.app/)**

---

## 📖 Como Adicionar um Novo Simulado (`simulado04.xlsx`, `simulado05.xlsx`...)

A plataforma conta com um leitor automático e genérico de planilhas. Adicionar uma nova avaliação não exige programação de arquivos `.html` adicionais.

### Passo 1: Enviar a planilha Excel para o GitHub
1. No repositório, clique em **Add file** > **Upload files**.
2. Envie o arquivo Excel no formato `.xlsx` padronizado (exemplo: `simulado04.xlsx`).
3. Clique em **Commit changes**.

### Passo 2: Adicionar a opção no `index.html` e `simulado.html`
1. No `index.html`, crie um novo cartão apontando para `simulado.html?prova=simulado04.xlsx`.
2. No `simulado.html`, adicione a linha `<option value="simulado04.xlsx">Simulado 04</option>` dentro da tag `<select id="selectSimuladoUrl">`.
