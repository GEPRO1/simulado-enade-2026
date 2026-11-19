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

---

## 🏆 Links Exclusivos — Simulado 02 Oficial (20/11/2026 • 13h00 às 17h00 • Ranking Top 3)

O **Simulado 02 (45 Questões Objetivas + 1 Discursiva — D1 + Questionário de Percepção P01–P09)** opera em **modo oficial restrito** com **data e janela travadas internamente no código para o dia 20/11/2026, das 13h00 às 17h00**, e **correção automática integral no padrão ENADE**:

* **Cálculo oficial ponderado ENADE (0 a 100 pontos):** **25%** Formação Geral (15 objetivas) + **75%** Componente Específico, subdividido em **85% Objetiva** (30 questões = 63,75% da nota final) e **15% Discursiva D1** (corrigida automaticamente pela rubrica analítica INEP = 11,25% da nota final);
* **Trava interna de data e horário (`20/11/2026`, `13h00` às `17h00`):** a data e o horário são definidos exclusivamente dentro do `simulado.html` (`CONFIG_SIMULADO02.dataOficial`), **não sendo editáveis pela URL**. O caderno é liberado automaticamente às **13h00**, exibe contador `Encerra às 17:00`, emite aviso aos **16h55** (5 minutos finais) e realiza o **envio automático às 17h00**;
* **Identificação & Código de Acesso (`GEPRO2026`):** exige Nome Completo, Apelido para o placar, Matrícula e Turma. Ao acessar pelo link oficial com `&acesso=GEPRO2026`, o código já é validado automaticamente e o campo fica oculto; caso o link seja aberto sem o parâmetro `&acesso=`, o sistema solicita o código **`GEPRO2026`**;
* **Questionário de Percepção da Prova (P01 a P09):** obrigatório antes da entrega final (sem pontuação, preenchido dentro do tempo total da prova, seguindo o rito oficial do INEP);
* **Segurança & Liberação após 4 horas:** durante a aplicação e nas 4 horas seguintes ao envio, ficam ocultos o gabarito comentado, Mapas Mentais, Matriz MEC, botão de impressão/`Ctrl+P` (exportação PDF), seleção/cópia dos enunciados e o ranking geral da turma. Decorridas **4 horas do envio**, o estudante pode reabrir o link e informar sua matrícula para revisar o caderno comentado e salvar em PDF;
* **Registro & Pódio Top 3:** grava horário de início, horário de término, duração, respostas por questão, resposta discursiva e percepção diretamente na planilha oficial no Google Sheets, destacando no painel docente o **pódio dos 3 primeiros colocados (maior nota geral ENADE e menor tempo de conclusão)**.

### 🔗 Links de Aplicação e Projeção (Simulado 02)

* 🎓 **Link Oficial para os Estudantes (`20/11/2026`, `13h00` às `17h00` • Código `GEPRO2026` já embutido):**
  `https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&acesso=GEPRO2026`
* 📊 **Painel de Projeção ao Vivo — Ranking Top 3 (por Apelido) & Dashboard da Turma (Uso Docente):**
  `https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&ranking=1`
* 🧪 **Link de Teste Docente (ignora a trava de data/horário para validação prévia):**
  `https://gepro1.github.io/simulado-enade-2026/simulado.html?prova=simulado02.xlsx&acesso=GEPRO2026&teste=1`

> **Como alterar a data ou horário em aplicações futuras:** como parâmetros de data na URL foram removidos por segurança, basta editar o objeto `CONFIG_SIMULADO02` diretamente no arquivo `simulado.html` no GitHub (`dataOficial: '2026-11-20'`, `horarioInicioPadrao: '13:00'`, `horarioTerminoPadrao: '17:00'`), mantendo exatamente o mesmo link para os estudantes.

---

## 🛠️ Arquitetura da Plataforma

O portal funciona em arquitetura aberta (*client-side* em HTML5, Tailwind CSS e SheetJS), integrada ao **Google Apps Script + Google Sheets** para coleta dos resultados oficiais do Simulado 02:

* `index.html` — Página inicial do portal com seleção dos cadernos de simulados livres e materiais de apoio.
* `simulado.html` — Motor único que lê qualquer planilha `.xlsx` padronizada, alternando automaticamente entre **Modo Treino Livre** (Simulados 01, 03 e 04) e **Modo Oficial Restrito** (Simulado 02, configurado para `20/11/2026`, das `13h00` às `17h00`).
* `simulado01.xlsx` — **Simulado 01 (Formação Geral):** Temas transversais contemporâneos (Sustentabilidade, ESG, Economia Circular, Direitos Humanos e LGPD).
* `simulado02.xlsx` — **Simulado 02 (Prova Oficial • 45 Objetivas + 1 Discursiva):** Caderno fechado no padrão INEP (15 FG + 30 CE objetivas + D1 discursiva autoavaliada) para aplicação supervisionada.
* `simulado03.xlsx` — **Simulado 03 (Aprofundamento):** Banco complementar de questões aplicadas.
* `simulado04.xlsx` — **Simulado 04 (Completo IV • 45Q + Discursiva):** Caderno inédito (15 FG + 30 CE) cobrindo todas as subáreas ABEPRO (Lean, CEP, Pesquisa Operacional, Engenharia Econômica e Ergonomia).

---

## 📖 Como Adicionar um Novo Simulado Livre (`simulado05.xlsx`...)

Não é necessário criar novos arquivos `.html`. O sistema lê automaticamente qualquer nova planilha enviada ao repositório:

### Passo 1: Enviar a planilha Excel para o GitHub
1. No repositório, clique em **Add file** > **Upload files**.
2. Envie o arquivo `.xlsx` seguindo o cabeçalho padrão (exemplo: `simulado05.xlsx`).
3. Clique em **Commit changes**.

### Passo 2: Vincular no `index.html` e no `simulado.html`
1. No **`index.html`**, adicione um cartão apontando para `simulado.html?prova=simulado05.xlsx`.
2. No **`simulado.html`**, inclua `<option value="simulado05.xlsx">Simulado 05</option>` dentro do menu `<select id="selectSimuladoUrl">`.

---

**Realização:** GEPRO — Laboratório de Gestão da Produção | Universidade Federal do Ceará (Campus de Russas).
