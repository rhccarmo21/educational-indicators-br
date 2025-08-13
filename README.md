# 📚 Educational Indicators BR

> **Resumo Executivo**  
> Integração de indicadores educacionais brasileiros com dados socioeconômicos para identificar desigualdades, monitorar desempenho escolar e mapear áreas prioritárias. Ferramenta essencial para gestores públicos, pesquisadores e analistas de dados que necessitam de análises georreferenciadas da educação básica no Brasil (2007-2023).

---

## 🚀 Fases de Desenvolvimento

### **Fase 1: Coleta e Preparação de Dados (Concluída ✅)**
- [x] Estrutura de diretórios criada (`data/raw`, `data/processed`, `scripts`)
- [x] Download dos microdados do INEP (2010-2024)
- [x] Scripts de extração automática de arquivos ZIP

### **Fase 2: Processamento Inicial (Em Andamento 🚧)**
- [ ] Processamento automatizado dos arquivos `ESCOLAS.CSV`
- [ ] Consolidação dos dados anuais em formato Parquet
- [ ] Tratamento de problemas de encoding e estrutura variável

### **Fase 3: Análise e Visualização (Próximos Passos 🔜)**
- [ ] Criação de dashboard Streamlit interativo
- [ ] Geração de mapas georreferenciados por município
- [ ] Desenvolvimento de relatórios automáticos em PDF

### **Fase 4: Modelagem Avançada (Planejada 📅)**
- [ ] Integração com dados socioeconômicos (IBGE)
- [ ] Modelos preditivos de desempenho escolar
- [ ] Análise de clusters para identificação de padrões

---

## 🚦 Roteiro de Execução Rápida

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
python scripts/process_censo.py  # Novo script padronizado

# 5. Iniciar dashboard
streamlit run app/streamlit/app.py

🛠️ Estrutura Atual do Projeto
edu-indicators-br/
├── data/
│   ├── raw/           # Microdados anuais (2010-2024)
│   ├── processed/     # Dados em Parquet por ano
│   └── consolidated/  # Dataset unificado
├── scripts/
│   ├── 1_extract_zips.py
│   ├── 2_process_escolas.py
│   └── 3_consolidate.py
├── app/
│   └── streamlit/     # Dashboard em desenvolvimento
└── notebooks/         # Análises exploratórias

📊 Próximos Marcos
Marco	Prazo	Status
Processamento completo	DD/MM/AAAA	🟡 Em andamento
Dashboard v1.0	DD/MM/AAAA	🟢 Planejado
Integração com dados IBGE	DD/MM/AAAA	🔴 Pendente
✨ Destaque das Novidades:

Pipeline automatizado de processamento de dados

Suporte a múltiplos encodings de arquivos

Documentação técnica ampliada em docs/

▶️ Comece agora | 📈 Ver métricas de exemplo
