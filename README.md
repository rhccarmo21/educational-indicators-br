# 📚 Educational Indicators BR

<div align="center">
  <img src="https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow" alt="Status">
  <img src="https://img.shields.io/badge/Python-3.9%2B-blue" alt="Python">
  <img src="https://img.shields.io/github/last-commit/rhccarmo21/educational-indicators-br" alt="Último commit">
</div>

> Plataforma de análise de indicadores educacionais com dados do INEP, IBGE e PNUD

---

## 🗂 Estrutura do Projeto

```text
📦 educational-indicators-br
├── 📂 app/               # Dashboard Streamlit
├── 📂 data/              # Dados
│   ├── raw/             # Brutos
│   └── processed/       # Processados
├── 📂 docs/              # Documentação
├── 📂 notebooks/         # Análises
├── 📂 outputs/           # Resultados
├── 📂 scripts/           # Automação
│   ├── extract_zips.sh
│   └── process_censo.py
├── 📂 tests/             # Testes
└── 📜 README.md          # Documentação
```

---

## 🚀 Fases do Projeto

### 1. 🏗️ Configuração (100%)
```progress
▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ 100%
```

### 2. 🧹 Processamento (75%)
```progress
▓▓▓▓▓▓▓▓▓▓▓▓▓░░░░░░░░░░░ 75%
```

### 3. 📊 Visualização (25%)
```progress
▓▓▓▓▓░░░░░░░░░░░░░░░░░░░ 25%
```

### 4. 🤖 Análise (0%)
```progress
░░░░░░░░░░░░░░░░░░░░░░░░░ 0%
```

---

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

## 📊 Indicadores

| Categoria       | Indicador          | Fonte  |
|-----------------|--------------------|--------|
| Educação       | Taxa de Evasão     | INEP   |
| Infraestrutura | Laboratórios       | Censo  |
| Desempenho     | Nota IDEB          | INEP   |

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

``` 

Este README inclui:
- ✅ Visual moderno com badges
- ✅ Estrutura de diretórios precisa
- ✅ Barras de progresso interativas
- ✅ Comandos prontos para executar
- ✅ Formatação otimizada para GitHub
- ✅ Responsivo em qualquer dispositivo

Para manter atualizado:
```bash
python scripts/update_readme.py
```
