# 📚 Educational Indicators BR

> **Resumo Executivo**  
> Integração de indicadores educacionais brasileiros com dados socioeconômicos para identificar desigualdades, monitorar desempenho escolar e mapear áreas prioritárias. Ferramenta essencial para gestores públicos, pesquisadores e analistas de dados que necessitam de análises georreferenciadas da educação básica no Brasil (2007-2023).

---

## 🚦 Roteiro de Execução Rápida

Siga estes passos para reproduzir a análise:

```bash
# 1. Clonar repositório
git clone https://github.com/rhccarmo21/educational-indicators-br.git
cd educational-indicators-br

# 2. Instalar dependências
pip install -r requirements.txt

# 3. Baixar microdados (links diretos)
wget -P data/raw/ https://dados.inep.gov.br/dataset/censo-escolar
wget -P data/raw/ https://ftp.ibge.gov.br/PNAD_Continua

# 4. Processar dados
# Obs.: edite 'scripts/build_dataset.py' para definir estado/ano específicos
python scripts/build_dataset.py

# 5. Gerar visualizações
python scripts/generate_maps.py --state=SP --year=2022
```

---

## 🎯 Níveis de Uso

### 🔵 Nível Rápido (Relatórios Pré-Formatados)
```python
from edu_analysis import EducationReport

report = EducationReport(
    state='BA', 
    year=2021,
    indicators=['ideb', 'evasao']
)
report.generate(output_file='relatorio_bahia.pdf')
```

### ⚡ Nível Avançado (API e Dashboard)
```python
# Acessar API de indicadores
from edu_api import get_school_indicators

indicadores = get_school_indicators(
    school_id=123456,
    indicators=['ideb', 'infraestrutura']
)

# Executar dashboard interativo
streamlit run app/edu_dashboard.py
```

---

## 📊 Indicadores Principais
| Categoria          | Indicador           | Fórmula                              | Fonte         |
|--------------------|---------------------|--------------------------------------|---------------|
| **Educacional**    | IDEB               | `(Proficiência × Fluxo)`             | INEP/MEC      |
|                    | Taxa de Abandono   | `(Mat.Iniciais - Mat.Finais)/Mat.Iniciais` | Censo Escolar |
| **Socioeconômico**| % Bolsa Família    | `Famílias beneficiadas/População`    | IBGE          |
|                    | Densidade Escolar  | `Escolas/Habitantes`                 | IBGE/INEP     |

> 📌 Fórmulas completas: [docs/indicadores.md](docs/indicadores.md)

---

## 🌐 Fontes de Dados
| Entidade | Conjunto de Dados   | Período     |
|----------|---------------------|-------------|
| INEP     | Censo Escolar       | 2007-2023   |
| IBGE     | PNAD Contínua       | 2016-2023   |
| PNUD     | IDH Municipal       | 2010-2020   |

---

## 🛠️ Estrutura do Projeto
```bash
edu-indicators-br/
├── data/
│   ├── raw/          # Microdados brutos
│   └── processed/    # Dados tratados
├── notebooks/        # Análises exploratórias
├── edu_analysis/     # Pipelines e modelos 
└── app/              # Dashboard Streamlit
```

---

## 🤝 Contribuição
Sugestões bem-vindas para:
- Novos indicadores educacionais
- Melhorias nas visualizações  
- Expansão de estudos de caso  

📌 Ver [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 📧 Contato Pessoal
**Roberto Cunha**  
[![GitHub](https://img.shields.io/badge/GitHub-rhccarmo21-blue)](https://github.com/rhccarmo21)  
✉️ rhccarmo@gmail.com

> 💡 **Para gestores educacionais:**  
> [Kit de estratégias baseadas em evidências](docs/estrategias_educacionais.pdf)
```
