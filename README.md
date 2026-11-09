# 🎓 Portal de Simulados ENADE — Engenharia de Produção

Plataforma web interativa desenvolvida para apoiar a preparação dos estudantes do curso de **Engenharia de Produção** da **Universidade Federal do Ceará (Campus Russas)** para o **ENADE 2026**.

---

## 🚀 Link de Acesso Público

O acesso é gratuito, universal e funciona em computadores, tablets e celulares sem necessidade de instalação:

👉 **[Acessar o Portal de Simulados](https://gepro1.github.io/simulado-enade-2026/)**


---
<!-- ------------------------------------------------------------- -->
<!-- ITEM 02: NOVO SIMULADO (ARQUIVO: 02.html)                     -->

## 📖 Como Adicionar um Novo Simulado (`02.html`, `03.html`...)

Para incluir uma nova avaliação no portal sem quebrar o link principal, siga os passos abaixo:

### Passo 1: Enviar o novo arquivo para o GitHub
1. No repositório, clique no botão **Add file** > **Upload files**.
2. Escolha o arquivo `.html` do novo simulado.
3. Defina um nome curto para o arquivo (exemplo: `02.html`).
4. Clique em **Commit changes**.

### Passo 2: Vincular o novo simulado no Portal (`index.html`)
1. Abra o arquivo `index.html` no GitHub e clique no ícone de **Lápis (Edit file)**.
2. Dentro da tag `<nav class="space-y-3.5 text-left">`, copie e cole o bloco de código abaixo:

```html
<!-- ------------------------------------------------------------- -->
<!-- ITEM 02: NOVO SIMULADO (ARQUIVO: 02.html)                     -->
<!-- ------------------------------------------------------------- -->
<a href="02.html" 
   class="group flex items-center justify-between p-4 rounded-xl border border-slate-200 bg-white hover:bg-ufcnavy-700 text-slate-800 hover:text-white transition-all duration-200 shadow-sm hover:shadow-md focus:outline-none focus:ring-2 focus:ring-ufcnavy-500">
    <div class="flex items-center space-x-3.5">
        <div class="w-10 h-10 rounded-lg bg-slate-100 group-hover:bg-white text-slate-700 group-hover:text-ufcnavy-700 flex items-center justify-center font-bold text-sm transition-colors">
            02
        </div>
        <div>
            <div class="flex items-center space-x-2">
                <h3 class="font-bold text-sm">Simulado Módulo II — Qualidade & PCP</h3>
                <span class="bg-blue-500 text-white text-[9px] font-bold px-1.5 py-0.5 rounded uppercase">Novo</span>
            </div>
            <p class="text-xs text-slate-500 group-hover:text-slate-200 transition-colors">15 Questões Objetivas</p>
        </div>
    </div>
    <i class="fa-solid fa-chevron-right text-slate-400 group-hover:text-white transition-transform group-hover:translate-x-1"></i>
</a>

# Simulado ENADE 2026 — Engenharia de Produção

Aplicação web interativa para preparação dos estudantes de Engenharia de Produção da UFC Campus Russas para a avaliação do ENADE 2026.

### 🚀 Link de Acesso ao Aplicativo:
Clique no link abaixo para acessar a plataforma:
👉 [Acessar o Simulado ENADE 2026] https://gepro1.github.io/simulado-enade-2026/
