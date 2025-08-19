# 📊 Projeto Educational Indicators BR

Este projeto tem como objetivo **integrar e analisar indicadores educacionais brasileiros com dados socioeconômicos**, transformando números em insights sobre desempenho escolar, desigualdades e o sistema educacional brasileiro.

🔗 [Acesse os microdados do INEP](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados)

---

## 🎯 Objetivos

### Para leigos
- Identificar quem está dentro e quem está fora da escola.
- Entender se os alunos estão aprendendo o que deveriam.
- Comparar escolas públicas e privadas.
- Mapear desigualdades regionais.
- Observar trajetórias do ensino básico ao superior.

### Para técnicos
- Criar pipelines de dados robustos para microdados massivos.
- Integrar múltiplas bases: Censo Escolar, Enem, Enade, Encceja e Censo Superior.
- Desenvolver análises exploratórias, visualizações e dashboards.
- Gerar comparações longitudinais (pré-teste com base 2022) e regionais.

---

## 📂 Estrutura de Diretórios

```bash
educational-indicators-br/
├── data/
│   ├── raw/             # Microdados originais do INEP e dados socioeconômicos
│   ├── interim/         # Dados processados parcialmente
│   └── processed/       # Bases finais prontas para análise
│
├── notebooks/           # Notebooks de análise exploratória e modelagem
│
├── src/                 # Scripts de ETL e análise
│   ├── download_data.py  # Script para baixar microdados
│   ├── preprocess.py     # Limpeza e padronização
│   └── analysis.py       # Funções de análise
│
├── reports/             # Relatórios e visualizações
│   └── figures/          # Gráficos e imagens
│
├── README.md            # Documentação do projeto
└── LICENSE              # Licença do projeto
```

---

## 📦 Microdados Utilizados

**Pré-teste (base 2022):**
- **Censo da Educação Superior**
- **Censo Escolar**
- **Enade**
- **Enem**
- **Encceja**

**Dados socioeconômicos confiáveis para séries históricas:**
- **Renda per capita municipal (IBGE)** — série longa e organizada: [IBGE - Estatísticas](https://www.ibge.gov.br/estatisticas/downloads-estatisticas.html)
- **IDH Municipal (PNUD/Atlas Brasil)** — série consolidada e confiável: [Atlas do Desenvolvimento Humano](http://www.atlasbrasil.org.br/acervo/biblioteca)

*(Em versões futuras, poderão ser incorporados dados do SAEB, ANA, Talis e outros indicadores socioeconômicos.)*

---

## ❓ Questões que Podem Ser Respondidas

- Como evoluiu a matrícula no ensino básico e superior?
- Quais padrões regionais de desempenho no Enem, Enade e Encceja?
- Existe relação entre infraestrutura escolar e desempenho dos alunos?
- Como o acesso ao ensino superior varia por região, rede e curso?
- Quais desigualdades aparecem nos indicadores educacionais por território?

---

## 🗓️ Cronograma

- **Fase 1:** Coleta de microdados (INEP)
- **Fase 2:** Limpeza e padronização
- **Fase 3:** Análises exploratórias (EDA)
- **Fase 4:** Construção de indicadores e visualizações
- **Fase 5:** Modelagem estatística e preditiva
- **Fase 6:** Relatórios e documentação

---

## ▶️ Como Executar o Projeto

1. **Clonar o repositório**
```bash
git clone https://github.com/rhccarmo21/educational-indicators-br.git
cd educational-indicators-br
```

2. **Criar e ativar ambiente virtual**
```bash
python3 -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

3. **Instalar dependências**
```bash
pip install -r requirements.txt
```

4. **Baixar microdados do INEP e dados socioeconômicos**
- Salve os arquivos ZIP na pasta `data/raw/`.

5. **Executar pré-processamento**
```bash
python src/preprocess.py
```

6. **Abrir notebooks para análise**
```bash
jupyter notebook notebooks/
```

---

## 📌 Observações

- Projeto modular: futuras versões poderão incorporar séries históricas e indicadores socioeconômicos adicionais.
- LGPD: variáveis sensíveis estão protegidas, garantindo privacidade dos alunos.
- Reprodutibilidade: toda análise é documentada e versionada.

---

## 📬 Contato

👤 Desenvolvido por **Roberto Cunha**  
🔗 [GitHub](https://github.com/rhccarmo21)  
✉️ rhccarmo@gmail.com

---

**Resumo:** Este projeto organiza e analisa milhões de dados sobre escolas e estudantes no Brasil, revelando padrões de aprendizado, desigualdades e impacto de políticas educacionais, transformando dados brutos em insights acionáveis.

