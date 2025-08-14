## 📚 Educational Indicators BR — Inteligência de Dados para Decisões em Educação

Imagine que você possa, em poucos cliques, saber **onde a educação está avançando e onde está ficando para trás**, quais regiões precisam de atenção urgente e **quais políticas funcionaram de fato**.  

Este projeto foi desenvolvido para **secretários de estado, ministros, parlamentares, gestores municipais, técnicos de órgãos de controle e líderes educacionais** que precisam **agir com base em evidências** — e não apenas em impressões.  

Usando dados integrados do **INEP**, **IBGE** e **PNUD** (2010–2014), a plataforma responde a perguntas como:  

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

### 🎯 O que você terá em mãos

- **Painel Interativo** para análise por município, estado ou região.  
- **Modelos preditivos** para simular cenários e apoiar decisões.  
- **Relatórios claros** para orientar políticas públicas com base em evidências.  

> Mais que um projeto de ciência de dados, o **Educational Indicators BR** é uma **ferramenta de gestão estratégica**, feita para transformar números em ação.

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
