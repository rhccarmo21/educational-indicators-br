# 📊 Projeto de Dados Educacionais

Este projeto tem como objetivo analisar dados educacionais brasileiros a partir das bases oficiais disponibilizadas pelo **Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP)**.  
A proposta é consolidar diferentes conjuntos de dados em uma estrutura organizada, de fácil manipulação e com potencial de expansão para análises mais complexas no futuro.

---

## 🎯 Objetivos

- Organizar e centralizar dados educacionais em um único projeto.  
- Realizar análises exploratórias e comparativas entre diferentes bases do INEP.  
- Criar uma estrutura escalável, que permita a integração futura de variáveis socioeconômicas.  

---

## ❓ Questões que este projeto poderá responder

Com base exclusivamente nos **microdados do INEP** já incorporados ao projeto, algumas das perguntas que poderão ser investigadas são:

### 📊 Desempenho dos estudantes
- Como variam as notas do **Enem** por região, estado e rede de ensino (pública x privada)?
- Quais fatores escolares (infraestrutura, perfil docente, número de alunos) se relacionam com o desempenho no **Saeb** e no **Enade**?
- Há desigualdades de desempenho entre grupos sociais (gênero, raça/cor, nível socioeconômico)?

### 🎓 Acesso e permanência
- Como evoluiu a matrícula nos diferentes níveis de ensino segundo o **Censo Escolar** e o **Censo da Educação Superior**?
- Qual a taxa de participação no **Encceja** por faixa etária e perfil dos participantes?
- Existem padrões de evasão ou retenção identificáveis nos microdados do Censo?

### 🏫 Escolas e ambiente escolar
- Qual é a distribuição de professores por formação e vínculo, segundo o **Censo dos Profissionais do Magistério**?
- Existem diferenças significativas de infraestrutura entre escolas urbanas e rurais (**PNERA**, Censo Escolar)?
- O que os dados da **Pesquisa de Ações Discriminatórias** revelam sobre desigualdades no ambiente escolar?

### 🧑‍🏫 Perfil dos professores
- Qual o perfil formativo e socioeconômico dos professores no Brasil, segundo o **Censo do Magistério** e o **Talis**?
- Há indícios de relação entre condições de trabalho docente e resultados de aprendizagem dos estudantes?

---

## 🗂️ Bases de Dados Utilizadas

As bases de dados estão disponíveis na página oficial de microdados do INEP:  
👉 [Acessar Microdados INEP](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados)

### Conjuntos de dados selecionados:
- **ANA** – Avaliação Nacional da Alfabetização  
- **Censo da Educação Superior**  
- **Censo Escolar**  
- **Enade** – Exame Nacional de Desempenho de Estudantes  
- **Encceja** – Exame Nacional para Certificação de Competências de Jovens e Adultos  
- **Enem** – Exame Nacional do Ensino Médio  
- **Enem por Escola**  
- **IDD** – Indicador de Diferença entre os Desempenhos Observado e Esperado  
- **Pesquisa de Ações Discriminatórias no Âmbito Escolar**  
- **PNERA** – Pesquisa Nacional da Educação na Reforma Agrária  
- **Saeb** – Sistema de Avaliação da Educação Básica  
- **Talis** – Pesquisa Internacional sobre Ensino e Aprendizagem  
- **Censo dos Profissionais do Magistério**  

---

## 🗓️ Cronograma do Projeto

| Fase                        | Descrição                                                                 | Status |
|-----------------------------|---------------------------------------------------------------------------|--------|
| Estrutura do repositório    | Pastas principais (dados, notebooks, scripts, app)                        | ✅ |
| Coleta de microdados INEP   | Download 2010–2024: Censo Escolar, IDEB, Saeb, Enem, Enade, Encceja… mais demais microdados | ⬜ |
| Integração bases INEP       | Merge Censo + IDEB + Saeb + Enem + demais microdados                      | ⬜ |
| Notebook inicial (2010)     | Pipeline mínimo de processamento                                           | ✅ |
| Análise exploratória (EDA)  | Estatísticas, gráficos e visualizações iniciais                            | ⬜ |
| Estudos comparativos        | Rankings entre municípios, estados e escolas                               | ⬜ |
| Dashboards e relatórios     | Painéis interativos em Streamlit                                           | ⬜ |
| Automação 2010–2024         | Scripts para processar todos os anos                                       | ⬜ |
| Documentação final          | README e metodologia detalhada                                             | ⬜ |

---

## 🔮 Extensões Futuras

Este projeto, em versões futuras, poderá integrar também indicadores socioeconômicos como **Renda, IDH e Gini**, provenientes de fontes oficiais (IBGE, PNUD, IpeaData), com o objetivo de enriquecer as análises e permitir estudos de correlação entre desigualdade social e desempenho educacional.

---

## ⚙️ Estrutura do Projeto

```
📂 projeto-dados-educacionais
 ┣ 📂 data/                # Diretório para armazenamento dos microdados
 ┃ ┣ 📂 raw/              # Dados brutos (ZIPs originais do INEP)
 ┃ ┣ 📂 interim/          # Dados intermediários após pré-processamento
 ┃ ┗ 📂 processed/        # Dados finais prontos para análise
 ┣ 📂 notebooks/           # Notebooks de exploração e análise
 ┣ 📂 src/                 # Scripts auxiliares
 ┃ ┣ 📂 ingestion/        # Rotinas de ingestão de dados
 ┃ ┣ 📂 preprocessing/    # Limpeza e transformação
 ┃ ┣ 📂 analysis/         # Funções de análise e métricas
 ┃ ┗ 📂 visualization/    # Funções para gráficos e relatórios
 ┣ 📂 outputs/             # Resultados (tabelas, gráficos, modelos)
 ┃ ┣ 📂 figures/          # Visualizações geradas
 ┃ ┣ 📂 reports/          # Relatórios e sumários
 ┃ ┗ 📂 models/           # Modelos treinados (se aplicável)
 ┣ 📜 README.md            # Documentação do projeto
 ┗ 📜 requirements.txt     # Dependências do ambiente
```

---

## 👨‍💻 Autor

Projeto desenvolvido por **Roberto Cunha**, com foco em transparência, ciência de dados aplicada à educação e análise de políticas públicas.  
🔗 [GitHub - rhccarmo21](https://github.com/rhccarmo21)
