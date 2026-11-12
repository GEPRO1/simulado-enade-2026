# 🎓 Portal de Simulados & Guia ENADE 2026 — Engenharia de Produção (UFC Russas)

Ecossistema digital desenvolvido pelo **GEPRO (Laboratório de Gestão da Produção)** para apoiar a preparação dos estudantes concludentes do curso de **Engenharia de Produção** da **Universidade Federal do Ceará — Campus de Russas** para o **ENADE 2026**.

---

## 🚀 Links de Acesso do Ecossistema ENADE 2026

* 🌐 **Portal de Simulados Interativos (Site Público):** [gepro1.github.io/simulado-enade-2026](https://gepro1.github.io/simulado-enade-2026/)
* 🧭 **Aplicativo Guia & Trilha de Estudos (ENADE Compass):** [enade-compass-2026.lovable.app](https://enade-compass-2026.lovable.app/)
* 📄 **Cartilha Oficial ENADE 2026 (PDF):** [Acessar Cartilha em PDF](./cartilha-enade-2026.pdf) *(certifique-se de enviar o PDF com este nome para a raiz do repositório)*
* 💻 **Repositório de Código-Fonte (GitHub):** [github.com/GEPRO1/simulado-enade-2026](https://github.com/GEPRO1/simulado-enade-2026)

---

## 🛠️ Arquitetura da Plataforma

O portal funciona em arquitetura aberta (*client-side* em HTML5, Tailwind CSS e SheetJS), sem necessidade de servidor pago ou banco de dados externo:

* `index.html` — Página inicial do portal com seleção de simulados e materiais de apoio.
* `simulado.html` — Motor único e genérico que lê qualquer planilha `.xlsx` padronizada, exibe a Matriz MEC, cronômetro, Mapas Mentais por disciplina, gabarito comentado e versão de impressão em A4.
* `simulado01.xlsx`, `simulado02.xlsx`, `simulado03.xlsx` — Bancos de questões curados pelo GEPRO conforme as Portarias MEC nº 154, 163 e 276/2026.

---

## 📖 Como Adicionar um Novo Simulado (`simulado04.xlsx`, `simulado05.xlsx`...)

Não é necessário criar novos arquivos `.html`. O sistema lê automaticamente qualquer nova planilha enviada ao repositório:

### Passo 1: Enviar a planilha Excel para o GitHub
1. No repositório, clique em **Add file** > **Upload files**.
2. Envie o arquivo `.xlsx` seguindo o cabeçalho padrão (exemplo: `simulado04.xlsx`).
3. Clique em **Commit changes**.

### Passo 2: Vincular no `index.html` e no `simulado.html`
1. No **`index.html`**, adicione um cartão apontando para `simulado.html?prova=simulado04.xlsx`.
2. No **`simulado.html`**, inclua `<option value="simulado04.xlsx">Simulado 04</option>` dentro do menu `<select id="selectSimuladoUrl">`.

---

**Realização:** GEPRO — Laboratório de Gestão da Produção | Universidade Federal do Ceará (Campus de Russas).
