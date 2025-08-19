# 📊 Projeto de Dados Educacionais

Este projeto tem como objetivo analisar dados educacionais brasileiros a partir das bases oficiais disponibilizadas pelo **Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP)**.  
A proposta é consolidar diferentes conjuntos de dados em uma estrutura organizada, de fácil manipulação e com potencial de expansão para análises mais complexas no futuro.

---

## 🎯 Objetivos

- Organizar e centralizar dados educacionais em um único projeto.  
- Realizar análises exploratórias e comparativas entre diferentes bases do INEP.  
- Criar uma estrutura escalável, que permita a integração futura de variáveis socioeconômicas.  

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
