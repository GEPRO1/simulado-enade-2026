# 🎓 Portal de Simulados & Guia ENADE 2026 — Engenharia de Produção (UFC Russas)

Ecossistema digital desenvolvido pelo **GEPRO (Laboratório de Gestão da Produção)** para apoiar a preparação dos estudantes concludentes do curso de **Engenharia de Produção** da **Universidade Federal do Ceará — Campus de Russas** para o **ENADE 2026**.

---

## 🚀 Links Principais do Ecossistema ENADE 2026

* 🌐 **Portal Principal de Simulados (Página Inicial):** [gepro1.github.io/simulado-enade-2026](https://gepro1.github.io/simulado-enade-2026/)
* 🧭 **Aplicativo Guia & Trilha de Estudos (ENADE Compass):** [enade-compass-2026.lovable.app](https://enade-compass-2026.lovable.app/)
* 📄 **Cartilha Oficial ENADE 2026 (PDF):** [Acessar Cartilha em PDF](./ebook_1enade2026.pdf)
* 💻 **Repositório de Código-Fonte (GitHub):** [github.com/GEPRO1/simulado-enade-2026](https://github.com/GEPRO1/simulado-enade-2026)

---

## 📝 Links Diretos dos Simulados Livres (Treino & Revisão)

Os simulados livres oferecem **correção comentada imediata**, **Matriz de Referência MEC**, **Mapas Mentais por área** e **versão de impressão em A4**:

* 📘 **Simulado 01 — Formação Geral:**
  [https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado01.xlsx](https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado01.xlsx)
* 📗 **Simulado 03 — Aprofundamento Complementar:**
  [https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado03.xlsx](https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado03.xlsx)
* 📙 **Simulado 04 — Prova Completa IV (45 Questões + Discursiva):**
  [https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado04.xlsx](https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado04.xlsx)
* 📕 **Simulado 05 — Prova Completa V (45 Questões + Discursiva):**
  [https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado05.xlsx](https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado05.xlsx)

---

## 🏆 Links Exclusivos — Simulado 02 Oficial (Aplicação Avaliativa & Sorteio)

O **Simulado 02 (44 Questões Objetivas + 1 Discursiva — Q16)** opera em **modo oficial restrito**:
* Exige identificação do estudante (Nome Completo, Apelido para o placar, Matrícula e Turma) e **Código de Acesso**;
* Oculta gabarito comentado, Mapas Mentais, Matriz MEC, botão de impressão/`Ctrl+P` (exportação PDF) e seleção/cópia dos enunciados durante a aplicação;
* Registra horário de início, horário de término, duração, respostas por questão e resposta discursiva diretamente na planilha oficial no Google Sheets;
* Mantém o placar geral oculto para os estudantes durante a prova, preservando a expectativa para o sorteio de brindes.

### 🔗 Links de Aplicação e Projeção (Simulado 02)

* 🎓 **Link Direto para os Estudantes (com código de acesso `GEPRO2026`):**
  [https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&acesso=GEPRO2026](https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&acesso=GEPRO2026)
* ⏰ **Modelo com Janela de Horário Agendada e Encerramento Automático (`&inicio=` e `&fim=`):**
  ```text
  https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&acesso=GEPRO2026&inicio=2026-11-18T14:00&fim=2026-11-18T17:00
  ```
  *(Basta ajustar data e hora em `inicio` e `fim` no formato `AAAA-MM-DDTHH:MM`. O sistema avisa o horário de término na entrada, alerta quando faltam 5 minutos e envia automaticamente ao atingir o limite.)*
* 📊 **Painel de Projeção ao Vivo — Ranking (por Apelido) & Dashboard da Turma (Uso Docente / Sorteio):**
  [https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&ranking=1](https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&ranking=1)

---

## 🛠️ Arquitetura da Plataforma

O portal funciona em arquitetura aberta (*client-side* em HTML5, Tailwind CSS e SheetJS), integrada ao **Google Apps Script + Google Sheets** para coleta dos resultados oficiais do Simulado 02:

* `index.html` — Página inicial do portal com seleção dos cadernos de simulados livres e materiais de apoio.
* `simulado.html` — Motor único que lê qualquer planilha `.xlsx` padronizada, alternando automaticamente entre **Modo Treino Livre** (Simulados 01, 03, 04 e 05) e **Modo Oficial Restrito** (Simulado 02).
* `simulado01.xlsx` — **Simulado 01 (Formação Geral):** Temas transversais contemporâneos (Sustentabilidade, ESG, Economia Circular, Direitos Humanos e LGPD).
* `simulado02.xlsx` — **Simulado 02 (Prova Oficial • 44 Objetivas + 1 Discursiva):** Caderno fechado no padrão INEP (15 FG + 29 CE objetivas + Q16 discursiva) para aplicação supervisionada.
* `simulado03.xlsx` — **Simulado 03 (Aprofundamento):** Banco complementar de questões aplicadas.
* `simulado04.xlsx` — **Simulado 04 (Completo IV • 45Q + Discursiva):** Caderno inédito (15 FG + 30 CE) com foco em PCP, Operações, Logística, Engenharia Organizacional, Simulação e Sustentabilidade.
* `simulado05.xlsx` — **Simulado 05 (Completo V • 45Q + Discursiva):** Caderno inédito (15 FG + 30 CE) cobrindo todas as subáreas ABEPRO (Lean, CEP, Pesquisa Operacional, Engenharia Econômica e Ergonomia).

---

## 📖 Como Adicionar um Novo Simulado Livre (`simulado06.xlsx`...)

Não é necessário criar novos arquivos `.html`. O sistema lê automaticamente qualquer nova planilha enviada ao repositório:

### Passo 1: Enviar a planilha Excel para o GitHub
1. No repositório, clique em **Add file** > **Upload files**.
2. Envie o arquivo `.xlsx` seguindo o cabeçalho padrão (exemplo: `simulado06.xlsx`).
3. Clique em **Commit changes**.

### Passo 2: Vincular no `index.html` e no `simulado.html`
1. No **`index.html`**, adicione um cartão apontando para `simulado.html?prova=simulado06.xlsx`.
2. No **`simulado.html`**, inclua `<option value="simulado06.xlsx">Simulado 06</option>` dentro do menu `<select id="selectSimuladoUrl">`.

---

**Realização:** GEPRO — Laboratório de Gestão da Produção | Universidade Federal do Ceará (Campus de Russas).
