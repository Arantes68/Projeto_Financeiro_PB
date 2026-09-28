# 💰 Dashboard Financeiro com Fluxo de Caixa | Power BI

## 📖 Sobre o Projeto

Este projeto consiste no desenvolvimento de um **Dashboard Financeiro** utilizando **Microsoft Power BI**, com o objetivo de analisar a movimentação financeira de uma empresa por meio de indicadores estratégicos e visualizações interativas.

O dashboard permite acompanhar receitas, custos, despesas, lucro e fluxo de caixa, auxiliando na tomada de decisão através de análises dinâmicas.

---

# 🎯 Objetivos

O projeto foi desenvolvido para atender aos seguintes requisitos de negócio:

* Comparar a receita mensal com o mesmo período do ano anterior;
* Analisar receitas por tipo de conta;
* Visualizar pagamentos por tipo de conta;
* Analisar pagamentos por mês;
* Identificar os principais clientes por receita;
* Construir um Fluxo de Caixa utilizando gráfico de cascata;
* Disponibilizar uma visão detalhada do Fluxo de Caixa.

---

# 📂 Fonte dos Dados

As informações foram disponibilizadas através das seguintes fontes:

* 📄 Arquivos TXT
* 📊 Arquivos Excel
* ☁️ OneDrive

Período analisado:

* **A partir de 2017**

---

# 🛠 Tecnologias Utilizadas

* Microsoft Power BI Desktop
* Power Query
* Linguagem DAX
* Modelagem Dimensional (Star Schema)
* Microsoft Excel
* Figma

---

# ⚙️ Etapas do Desenvolvimento

## 1️⃣ Importação dos Dados

Os arquivos foram organizados localmente e importados para o Power BI Desktop.

Tabelas utilizadas:

* Cadastro
* Recebimentos
* Pagamentos

---

## 2️⃣ Tratamento dos Dados

Todo o processo de limpeza e transformação foi realizado no **Power Query**.

Entre as atividades realizadas estão:

* Padronização dos dados;
* Ajuste dos tipos de dados;
* Organização das tabelas;
* Preparação para a modelagem dimensional.

---

## 3️⃣ Criação da Dimensão Calendário

Foi criada uma tabela **dCalendario**, utilizada para análises temporais.

Principais atributos:

* Data
* Ano
* Nome do Mês
* Número do Mês
* Mês/Ano

---

## 4️⃣ Modelagem dos Dados

Foi adotado o modelo **Star Schema (Esquema Estrela)**, seguindo boas práticas de Business Intelligence para melhorar a organização e a performance do modelo.

### Tabelas Dimensão

* dCalendario
* dPlanoContas

### Tabelas Fato

* fRecebimentos
* fPagamentos

### Tabela de Medidas

* Medidas (DAX)

---

## 🔗 Relacionamentos

| Origem                       | Destino  | Status     |
| ---------------------------- | -------- | ---------- |
| dCalendario → fRecebimentos  | Data     | ✅ Ativo    |
| dCalendario → fPagamentos    | Data     | ✅ Ativo    |
| dPlanoContas → fRecebimentos | ID Conta | ✅ Ativo    |
| dPlanoContas → fPagamentos   | Conta    | ⚠️ Inativo |

Todos os relacionamentos utilizam:

* Cardinalidade **1:N**
* Filtragem unidirecional
* Modelo dimensional

---

# 📐 Medidas DAX

Durante o desenvolvimento foram criadas medidas utilizando funções como:

* SUM()
* CALCULATE()
* FILTER()
* DIVIDE()

## Principais indicadores

* Receitas
* Saídas
* Custos
* Despesas
* Margem Bruta
* Lucro
* % Lucro

---

# 📊 Dashboard

Para tornar o relatório mais profissional, foi desenvolvido um layout personalizado no **Figma**, posteriormente utilizado como plano de fundo do dashboard.

Após isso foram construídos os principais visuais.

### Indicadores

* Receita
* Custos
* Despesas
* Lucro
* Margem Bruta

### Visualizações

* Cartões (KPIs)
* Gráfico de Colunas
* Gráfico de Barras
* Gráfico de Cascata
* Tabelas
* Segmentação de Dados

---

# 🎛 Recursos Interativos

O dashboard possui recursos que facilitam a navegação e a análise dos dados.

### Segmentação

Filtro por:

* Ano

### Navegação

Botões personalizados para mudança entre páginas do relatório.

---

# 📁 Estrutura do Projeto

```text
📦 Dashboard-Financeiro-PowerBI
 ├── Base de Dados
 │    ├── Cadastro
 │    ├── Pagamentos
 │    └── Recebimentos
 │
 ├── Dashboard.pbix
 ├── README.md
 └── Imagens
      ├── Dashboard.png
      ├── FluxoCaixa.png
      └── Modelagem.png
```

---

# 📈 Principais Resultados

O dashboard permite responder rapidamente perguntas como:

* Qual foi a receita da empresa por período?
* Qual a evolução das receitas ao longo dos anos?
* Quanto foi gasto com custos e despesas?
* Qual o lucro obtido?
* Como está o fluxo de caixa?
* Quais clientes geraram maior receita?
* Qual tipo de conta possui maior movimentação financeira?

---

# 🚀 Competências Desenvolvidas

Durante este projeto foram aplicados conhecimentos em:

* Power BI
* Power Query
* Linguagem DAX
* Modelagem Dimensional
* Star Schema
* Business Intelligence
* Dashboards Gerenciais
* Análise Financeira
* Visualização de Dados
* Design de Dashboards

---

# 📸 Demonstração

> **Sugestão:** adicione capturas de tela do dashboard nesta seção para apresentar os principais indicadores e páginas do projeto.

```
📷 Dashboard Principal

(Imagem)

📷 Fluxo de Caixa

(Imagem)

📷 Modelagem dos Dados

(Imagem)
```

---

# 👨‍💻 Autor

**Marcos Vinicius**

Analista de Monitoramento (NOC) | Pós-graduando em Engenharia de Dados e Inteligência Artificial | Apaixonado por Business Intelligence, Engenharia de Dados e Análise de Dados.

**LinkedIn:** *(adicione o link)*

**GitHub:** *(adicione o link)*
