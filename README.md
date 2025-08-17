# 📚 Educational Indicators BR — Inteligência de Dados para Decisões em Educação

> **Transforme indicadores em ação.** Em poucos cliques, identifique onde a educação avança, onde está ficando para trás e quais políticas realmente funcionam.

---

## 🎯 Para quem é

Secretários(as) de Estado, ministros(as), parlamentares, gestores(as) municipais, técnicos(as) de órgãos de controle e lideranças educacionais que precisam agir com **evidências**, não apenas impressões.

---

## 🔍 O que você vai conseguir responder

- **Onde agir primeiro?** Municípios com maior evasão e queda de desempenho.
- **Infraestrutura importa?** Efeitos de bibliotecas, laboratórios e internet no IDEB.
- **Desigualdade e aprendizagem.** Efeito de renda per capita e desigualdade social no desempenho.
- **Impacto de políticas públicas.** Efeitos do Mais Educação, expansão de universidades e outros programas.
- **Desempenho regional comparado.** Quem avança mais rápido e por quê.
- **Projeções.** Se nada mudar, como estará o IDEB municipal nos próximos anos.
- **Caminhos para reverter a evasão.** Fatores que mais pesam na permanência/abandono.
- **Eficiência de investimento.** Onde o gasto educacional gera melhor retorno em aprendizagem.

---

## 🧠 Metodologia com IA (ChatGPT como copilot)

A IA é utilizada como **instrumento de desenvolvimento** e suporte técnico-metodológico; **todas as decisões, validações e interpretações são do pesquisador**.

- **Formulação de código:** criação de scripts/notebooks para processamento, integração e análise; pipelines incrementais com testes.
- **Suporte matemático/estatístico:** definição de métricas, variáveis e modelos; interpretação de resultados e cruzamentos.
- **Organização do projeto:** diretórios reprodutíveis; *naming conventions*; versionamento de datasets e saídas.
- **Análises e visualizações:** gráficos, dashboards e relatórios interpretativos, com foco em qualidade, desigualdades e fatores socioeconômicos.

> **Nota:** esta abordagem aumenta **precisão, escalabilidade e transparência** no ciclo de desenvolvimento.

---

## 🧱 Fontes de Dados (2010–2024)

Este projeto integra dados de diferentes fontes oficiais:

- **Censo Escolar (INEP):** [https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados)
- **IDEB (INEP):** [https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/indicadores-educacionais](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/indicadores-educacionais)
- **IBGE — Indicadores Socioeconômicos:** [https://www.ibge.gov.br/estatisticas/downloads-estatisticas.html](https://www.ibge.gov.br/estatisticas/downloads-estatisticas.html)
- **PNUD — Atlas do Desenvolvimento Humano (IDHM, Renda, Gini):** [http://www.atlasbrasil.org.br/acervo/biblioteca](http://www.atlasbrasil.org.br/acervo/biblioteca)

Fluxo (alto nível):

```
[Coleta Bruta ZIP] → [Validação/Schema] → [Normalização/Chaves IBGE] →
[Integração (Censo + IDEB + PNUD)] → [Camada Processed/Parquet] →
[Modelagem/EDA] → [Dashboards/Relatórios]
```

Chaves de integração principais:

- **IBGE município (7 dígitos)** e **UF**
- **Ano de referência**
- **Identificadores de escola** (quando aplicável)

---

## 🗂 Estrutura do Projeto

```
📦 educational-indicators-br
├── 📂 app/               # Dashboard Streamlit
├── 📂 data/              # Dados
│   ├── raw/              # Brutos
│   └── processed/        # Processados (Parquet/CSV)
├── 📂 docs/              # Documentação
├── 📂 notebooks/         # Análises exploratórias e modelagem
├── 📂 outputs/           # Resultados e relatórios
├── 📂 scripts/           # Automação
│   ├── extract_zips.sh
│   └── process_censo.py
├── 📂 tests/             # Testes
└── 📜 README.md          # Você está aqui
```

---

## ⚡ Instalação e Uso

```bash
# Clonar o repositório
git clone https://github.com/rhccarmo21/educational-indicators-br.git
cd educational-indicators-br

# Criar ambiente
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Instalar dependências
pip install -r requirements.txt

# (opcional) Instalar em modo dev
pip install -e .
```

### 📦 Processar dados

```bash
# Extrair ZIPs de dados brutos
./scripts/extract_zips.sh

# Processar Censo Escolar (ex.: 2010)
python scripts/process_censo.py --year 2010 --input data/raw --output data/processed
```

### 🖥️ Executar o dashboard

```bash
streamlit run app/app.py
```

---

## 📊 Indicadores Monitorados

Tabela-base para diagnósticos, comparações e projeções.

| Categoria      | Indicador                             | Fonte         | O que revela                                  |
| -------------- | ------------------------------------- | ------------- | --------------------------------------------- |
| Educação       | **Taxa de Evasão**                    | INEP          | Permanência e risco de abandono escolar       |
| Infraestrutura | **Bibliotecas/Laboratórios/Internet** | Censo Escolar | Condições materiais favoráveis à aprendizagem |
| Desempenho     | **IDEB (Iniciais/Finais/EM)**         | INEP          | Qualidade do ensino (fluxo + desempenho)      |
| Socioeconômico | **Renda per capita / Gini / IDHM**    | IBGE / PNUD   | Contexto social e desigualdades               |

> Esses indicadores, combinados, ajudam a priorizar intervenções, avaliar políticas e otimizar recursos públicos.

---

## 🚦 Status & Roadmap

| Fase                          | Descrição                                                            | Status |
| ----------------------------- | -------------------------------------------------------------------- | ------ |
| Estrutura do repositório      | Pastas principais (Censo, IDEB, PNUD, notebooks, scripts, processed) | ✅      |
| Coleta Censo Escolar          | Download 2010–2024                                                   | ✅      |
| Coleta IDEB                   | Download 2010–2024                                                   | ⬜      |
| Coleta PNUD/IBGE              | Download 2010–2024                                                   | ⬜      |
| Organização de dados          | Subpastas por ano                                                    | ⬜      |
| Notebook inicial (2010)       | Pipeline mínimo de processamento                                     | ✅      |
| Integração de datasets        | Merge Censo + IDEB + PNUD                                            | ⬜      |
| Análise exploratória (EDA)    | Estatísticas, gráficos e visualizações iniciais                      | ⬜      |
| Estudos comparativos/rankings | Comparações entre escolas, municípios e estados                      | ⬜      |
| Dashboards e relatórios       | Painéis e relatórios consolidados                                    | ⬜      |
| Automação (2010–2024)         | Scripts para processar todos os anos                                 | ⬜      |
| Documentação final            | README e metodologia detalhada                                       | ⬜      |

Checklist (curto prazo):

-

---

## 🧪 Qualidade & Testes

- **Validação de schema** (tipos, nulidade, *ranges*) com testes em `tests/`.
- **Checks de integridade**: contagens por UF/ano; chaves duplicadas; cobertura de escolas.
- **Reprodutibilidade**: versões de dados no nome do arquivo e *hash* de origem.

---

## 🧩 Modelagem & Cenários

- **Projeções de IDEB** por município/etapa via modelos de séries temporais e regressão (baseline: ARIMA/ETS; extensões: Prophet/Random Forest/LightGBM).
- **Evasão escolar**: modelos explicativos com *feature importance* (SHAP) para orientar políticas.
- **Eficiência de investimento**: análise de produtividade (DEA/Frontier) e correlação gasto→resultado.

> Os resultados são explicáveis e acompanhados de métricas (MAPE/RMSE/AUC) e análise de viés.

---

## 🛡️ Ética, Transparência e Limites

- **Dados públicos** e documentação de origem.
- **Rastreabilidade**: código aberto, *versioning* de insumos e outputs.
- **Privacidade**: agregações adequadas; sem dados pessoais sensíveis.
- **Limitações**: indicadores não capturam toda a complexidade pedagógica; resultados devem ser interpretados com especialistas.

---

## 🤝 Como Contribuir

1. Abra uma *issue* com o prefixo `[BUG]`, `[FEATURE]` ou `[DOCS]`.
2. Crie uma *branch* a partir de `main`.
3. Envie um PR com descrição clara, *screenshots* e checklist de testes.

Atalhos:

```bash
# Reportar bug (exemplo)
git issue new -t "[BUG] descrição do problema"
```

---

## 📄 Licença

Defina a licença do projeto (ex.: MIT). Adicione o arquivo `LICENSE` na raiz.

---

## 📬 Contato

- GitHub: **@rhccarmo21**
- Issues: use o repositório para dúvidas e sugestões
- (Opcional) E-mail/LinkedIn do mantenedor

