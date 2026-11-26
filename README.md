# 🎓 Portal de Simulados & Guia ENADE 2026 — Engenharia de Produção (UFC Russas)

Ecossistema digital desenvolvido pelo **GEPRO (Laboratório de Gestão da Produção)** para apoiar a preparação dos estudantes concludentes do curso de **Engenharia de Produção** da **Universidade Federal do Ceará — Campus de Russas** para o **ENADE 2026**.

---

## 🚀 Links Principais do Ecossistema ENADE 2026

* 🌐 **Portal Principal de Simulados (Página Inicial):** [gepro1.github.io/simulado-enade-2026](https://gepro1.github.io/simulado-enade-2026/)
* 🧭 **Aplicativo Guia & Trilha de Estudos (ENADE Compass):** [enade-compass-2026.lovable.app](https://enade-compass-2026.lovable.app/)
* ✍️ **Oficina Plus de Questões Discursivas (Estudos de Caso):** [gepro1.github.io/simulado-enade-2026/discursivas.html](https://gepro1.github.io/simulado-enade-2026/discursivas.html)
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

---

## 🏆 Links Exclusivos — Simulado 05 Oficial (27/11/2026 • 13h00 às 17h00 • Ranking Top 3)

O **Simulado 05 (45 Questões Objetivas + Discursiva + Questionário de Percepção P01–P09)** opera em **modo oficial restrito** com **data e janela travadas internamente no código para o dia 27/11/2026, das 13h00 às 17h00**, e **correção automática integral no padrão ENADE**:

* **Cálculo oficial ponderado ENADE (0 a 100 pontos):** **25%** Formação Geral (15 objetivas) + **75%** Componente Específico, subdividido em **85% Objetiva** (30 questões = 63,75% da nota final) e **15% Discursiva** (11,25% da nota final);
* **Trava interna de data e horário (`27/11/2026`, `13h00` às `17h00`):** o caderno é liberado automaticamente às **13h00**, exibe contador `Encerra às 17:00`, emite aviso aos **16h55** (5 minutos finais) e realiza o **envio automático às 17h00**;
* **Identificação & Código de Acesso (`GEPRO2026`):** exige Nome Completo, Apelido para o placar, Matrícula e Turma;
* **Segurança & Liberação após 4 horas:** durante a aplicação e nas 4 horas seguintes ao envio, ficam ocultos o gabarito comentado, Mapas Mentais, Matriz MEC, botão de impressão/`Ctrl+P` (exportação PDF), seleção/cópia dos enunciados e o ranking geral da turma. Decorridas **4 horas do envio**, o estudante pode reabrir o link e informar sua matrícula para revisar o caderno comentado e salvar em PDF;
* **Registro & Pódio Top 3:** grava horário de início, horário de término, duração, respostas por questão, resposta discursiva e percepção diretamente na planilha oficial no Google Sheets.

### 🔗 Links de Aplicação e Projeção (Simulado 05 — 27/11/2026)

* 🎓 **Link Oficial para os Estudantes (`27/11/2026`, `13h00` às `17h00` • Código `GEPRO2026` já embutido):**
  `https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado05.xlsx&acesso=GEPRO2026`
* 📊 **Painel de Projeção ao Vivo — Ranking Top 3 (por Apelido) & Dashboard da Turma (Uso Docente):**
  `https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado05.xlsx&ranking=1`
* 🧪 **Link de Teste Docente (ignora a trava de data/horário para validação prévia):**
  `https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado05.xlsx&acesso=GEPRO2026&teste=1`

### 🔗 Links Históricos — Simulado 02 Oficial (20/11/2026)

* 🎓 **Link Oficial dos Estudantes:** `https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&acesso=GEPRO2026`
* 📊 **Ranking Top 3 & Dashboard (Simulado 02):** `https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&ranking=1`

---

## 🛠️ Arquitetura da Plataforma

O portal funciona em arquitetura aberta (*client-side* em HTML5, Tailwind CSS e SheetJS), integrada ao **Google Apps Script + Google Sheets** para coleta dos resultados oficiais:

* `index.html` — Página inicial do portal com seleção dos cadernos de simulados livres, acesso à Oficina Discursiva e status das provas oficiais restritas.
* `simulado.html` — Motor único que lê qualquer planilha `.xlsx` padronizada, alternando automaticamente entre **Modo Treino Livre** (Simulados 01, 03 e 04) e **Modo Oficial Restrito** (Simulados 02 e 05).
* `discursivas.html` — **Oficina Plus de Questões Discursivas:** 5 estudos de caso inéditos da área específica com folha oficial de 30 linhas, envio de foto manuscrita, protocolo de banca avaliadora e folha de impressão A4.
* `simulado01.xlsx` — **Simulado 01 (Formação Geral):** Temas transversais contemporâneos.
* `simulado02.xlsx` — **Simulado 02 (Prova Oficial I • 20/11/2026):** Caderno fechado no padrão INEP.
* `simulado03.xlsx` — **Simulado 03 (Aprofundamento):** Banco complementar de questões aplicadas.
* `simulado04.xlsx` — **Simulado 04 (Completo IV • 45Q + Discursiva):** Caderno inédito cobrindo todas as subáreas ABEPRO.
* `simulado05.xlsx` — **Simulado 05 (Prova Oficial II • 27/11/2026):** Caderno inédito fechado (15 FG + 30 CE) com 17 gráficos e diagramas técnicos.

---

**Realização:** GEPRO — Laboratório de Gestão da Produção | Universidade Federal do Ceará (Campus de Russas).
