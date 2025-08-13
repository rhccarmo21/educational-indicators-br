# 📚 Educational Indicators BR

> **Resumo Executivo**  
> Integração de indicadores educacionais brasileiros com dados socioeconômicos para identificar desigualdades, monitorar desempenho escolar e mapear áreas prioritárias. Ferramenta essencial para gestores públicos, pesquisadores e analistas de dados que necessitam de análises georreferenciadas da educação básica no Brasil (2007-2023).

---

## 🌟 Fases de Desenvolvimento

### **Fase 1: Coleta de Dados** ✅
```text
✔️ Estrutura de diretórios criada  
✔️ Download dos microdados (2010-2024)  
✔️ Scripts de extração automática  
```

### **Fase 2: Processamento** 🚧
```text
◻ Processamento dos arquivos ESCOLAS.CSV  
◻ Consolidação em formato Parquet  
◻ Tratamento de encoding variável  
```

### **Fase 3: Análise** 🔜
```text
◻ Dashboard interativo (Streamlit)  
◻ Mapas georreferenciados  
◻ Relatórios automáticos em PDF  
```

### **Fase 4: Modelagem** 📅
```text
◻ Integração com dados IBGE  
◻ Modelos preditivos de desempenho  
◻ Análise de clusters  
```

---

## 🚀 Como Usar

### **Instalação**
```bash
git clone https://github.com/rhccarmo21/educational-indicators-br.git
cd educational-indicators-br
pip install -r requirements.txt
```

### **Processamento de Dados**
```bash
# Extrair arquivos ZIP
python scripts/1_extract_zips.py

# Processar dados escolares
python scripts/2_process_escolas.py

# Consolidar dados anuais
python scripts/3_consolidate.py
```

### **Visualização**
```bash
# Iniciar dashboard
streamlit run app/streamlit/app.py
```

---

## 🗂 Estrutura do Projeto
```
.
├── data/
│   ├── raw/              # Dados brutos por ano
│   ├── processed/        # Dados processados (Parquet)
│   └── consolidated/     # Dataset unificado
├── scripts/
│   ├── 1_extract_zips.py # Extração de arquivos
│   ├── 2_process.py      # Pipeline de ETL
│   └── 3_consolidate.py  # Consolidação
└── app/
    └── streamlit/        # Dashboard interativo
```

---

## 📊 Indicadores Principais
| Categoria          | Indicador         | Fonte        |
|--------------------|-------------------|-------------|
| **Educacional**    | IDEB              | INEP        |
|                    | Taxa de Evasão    | Censo Escolar |
| **Socioeconômico** | % Bolsa Família   | IBGE        |

---

## 📌 Próximos Passos
1. [ ] Finalizar processamento dos dados de 2022
2. [ ] Implementar filtros no dashboard
3. [ ] Adicionar geolocalização das escolas

---

## 🤝 Como Contribuir
1. Faça um fork do projeto
2. Crie um branch (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Add feature'`)
4. Push para o branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

---

## 📧 Contato
**Roberto Cunha**  
[![Github](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rhccarmo21)  
✉️ rhccarmo@gmail.com
```
