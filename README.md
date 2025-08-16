## 📚 Educational Indicators BR — Inteligência de Dados para Decisões em Educação

Imagine que você possa, em poucos cliques, saber **onde a educação está avançando e onde está ficando para trás**, quais regiões precisam de atenção urgente e **quais políticas funcionaram de fato**.  

Este projeto foi desenvolvido para **secretários de estado, ministros, parlamentares, gestores municipais, técnicos de órgãos de controle e líderes educacionais** que precisam **agir com base em evidências** — e não apenas em impressões.  

Usando dados integrados do **INEP**, **IBGE** e **PNUD** (2010–2024), a plataforma responde a perguntas como:  

---

### 🔍 Perguntas Estratégicas que Você Poderá Responder

1. **Onde agir primeiro?**  
   Quais municípios concentram os maiores índices de evasão escolar e queda de desempenho?  

2. **Infraestrutura importa?**  
   Escolas com bibliotecas, laboratórios e internet têm evolução significativa no IDEB?  

3. **Desigualdade e aprendizagem**  
   Como renda per capita e desigualdade social afetam o desempenho dos estudantes?  

4. **Impacto de políticas públicas**  
   O Mais Educação, a expansão de universidades e outros programas tiveram efeito mensurável?  

5. **Desempenho regional comparado**  
   Quais regiões estão avançando mais rápido e por quê?  

6. **Projeções para o futuro**  
   Se nada mudar, como estará o IDEB de cada município nos próximos anos?  

7. **Caminhos para reverter a evasão**  
   Quais fatores mais pesam na permanência ou abandono escolar?  

8. **Eficiência de investimento**  
   Onde o gasto educacional trouxe melhor retorno em resultados de aprendizagem?  

---
## Metodologia

O desenvolvimento deste projeto segue uma metodologia orientada por **Inteligência Artificial**, utilizando o ChatGPT como ferramenta de suporte estratégico, conceitual e prática em diversas etapas:

1. **Formulação de código**  
   - Criação de scripts e notebooks para processamento, integração e análise de dados.
   - Desenvolvimento incremental de pipelines, com validação e teste de cada etapa.

2. **Suporte matemático e estatístico**  
   - Auxílio na definição de métricas, variáveis e modelos explicativos.
   - Orientação na interpretação de resultados, cruzamentos de dados e análises estatísticas.

3. **Organização do projeto**  
   - Estruturação de diretórios e arquivos de forma clara e replicável.
   - Padronização de naming conventions, versão de datasets e arquivos de saída.

4. **Desenvolvimento de análises e visualizações**  
   - Criação de gráficos, dashboards e relatórios interpretativos.
   - Facilitação de insights sobre qualidade educacional, desigualdades e correlações com fatores socioeconômicos.

> 💡 Nota: A IA é utilizada como **instrumento de desenvolvimento**, fornecendo suporte técnico e metodológico, mas todas as decisões finais, validações e interpretações ficam sob responsabilidade do pesquisador. Esta abordagem garante precisão, escalabilidade e transparência na construção do projeto.

---

### 🎯 O que você terá em mãos

- **Painel Interativo** para análise por município, estado ou região.  
- **Modelos preditivos** para simular cenários e apoiar decisões.  
- **Relatórios claros** para orientar políticas públicas com base em evidências.  

> Mais que um projeto de ciência de dados, o **Educational Indicators BR** é uma **ferramenta de gestão estratégica**, feita para transformar números em ação.

---

## Fases do Projeto

| Fase | Descrição | Status |
|------|-----------|--------|
| Estrutura do repositório | Criação das pastas principais (Censo Escolar, IDEB, PNUD, notebooks, scripts, dados processados) | ✅ Concluído |
| Coleta de dados Censo Escolar | Download da base completa 2010–2024 | ✅ Concluído |
| Coleta de dados IDEB | Download da base completa 2010–2024 | ⬜ Pendente |
| Coleta de dados PNUD | Download da base completa 2010–2024 | ⬜ Pendente |
| Organização de dados | Preparação da estrutura de subpastas por ano | ⬜ Pendente |
| Notebook de processamento inicial | Desenvolvimento do notebook para o ano de 2010 | ✅ Concluído |
| Integração de datasets | Merge entre Censo Escolar, IDEB e PNUD | ⬜ Pendente |
| Análise exploratória | Estatísticas descritivas, gráficos e visualizações iniciais | ⬜ Pendente |
| Estudos comparativos e rankings | Comparações entre escolas, municípios e estados | ⬜ Pendente |
| Dashboards e relatórios | Desenvolvimento de dashboards e relatórios consolidados | ⬜ Pendente |
| Automação do processamento | Scripts para processar automaticamente todos os anos 2010–2024 | ⬜ Pendente |
| Documentação final | Atualização do README e metodologia detalhada | ⬜ Pendente |

---

## 🗂 Estrutura do Projeto

```text
📦 educational-indicators-br
├── 📂 app/               # Dashboard Streamlit
├── 📂 data/              # Dados
│   ├── raw/              # Brutos
│   └── processed/        # Processados
├── 📂 docs/              # Documentação
├── 📂 notebooks/         # Análises
├── 📂 outputs/           # Resultados
├── 📂 scripts/           # Automação
│   ├── extract_zips.sh
│   └── process_censo.py
├── 📂 tests/             # Testes
└── 📜 README.md          # Documentação
```

## ⚡ Como Usar

```bash
# Clonar e instalar
git clone https://github.com/rhccarmo21/educational-indicators-br.git
cd educational-indicators-br
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Processar dados
./scripts/extract_zips.sh
python scripts/process_censo.py

# Executar dashboard
streamlit run app/app.py
```

---

## 📊 Indicadores Monitorados

Os indicadores abaixo são a base para diagnósticos, comparações e projeções estratégicas.  
Eles foram selecionados por seu **alto poder explicativo** sobre a qualidade e os resultados da educação no Brasil.

| Categoria       | Indicador                        | Fonte  | O que Revela |
|-----------------|----------------------------------|--------|--------------|
| **Educação**    | **Taxa de Evasão**               | INEP   | Mede a permanência dos estudantes na escola e identifica risco de abandono escolar. |
| **Infraestrutura** | **Presença de Laboratórios e Bibliotecas** | Censo Escolar | Avalia condições materiais que favorecem a aprendizagem e o desenvolvimento científico. |
| **Desempenho**  | **Nota IDEB**                    | INEP   | Indicador-síntese da qualidade do ensino, combinando fluxo escolar e desempenho em avaliações padronizadas. |

> Esses indicadores, quando analisados em conjunto com dados socioeconômicos (IBGE, PNUD), permitem identificar **onde intervir primeiro**, **quais políticas funcionam** e **como otimizar recursos públicos**.

---

## 🤝 Contribua

1. Reporte bugs:
```bash
git issue new -t "[BUG] Descrição"
```

2. Envie melhorias:
```bash
git flow feature start minha-feature
```

---

<div align="center">
📧 **Contato**: rhccarmo@gmail.com  
🔗 **Repositório**: github.com/rhccarmo21/educational-indicators-br
</div>

---

> 💡 Use `make help` para ver comandos disponíveis
```bash
make process  # Pipeline completo
make test     # Executar testes
```


