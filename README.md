# 📊 Análise de Cancelamento de Clientes (Churn Analysis)

Este projeto tem como objetivo analisar os **fatores que levam clientes a cancelar serviços** e propor **ações estratégicas para reduzir a taxa de churn**.  
A análise foi feita em **Python** através de um Jupyter Notebook, explorando a base de dados `cancelamentos.csv`.

---

## 🚀 Objetivos do Projeto


```
- Entender o perfil dos clientes que cancelaram.  
- Identificar padrões e principais causas de cancelamento.  
- Criar **gráficos dinâmicos e interativos** para apoiar a análise.  
- Propor ações práticas para diminuir a taxa de churn.  
```


---

## 📂 Estrutura do Projeto

```
📦 projeto-automacao
 ┣ 📜 inicial.ipynb      # Notebook principal com toda a análise
 ┣ 📜 cancelamentos.csv  # Base de dados dos clientes
 ┗ 📜 README.md          # Documentação do projeto
```

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- [Pandas](https://pandas.pydata.org/) → Manipulação e limpeza da base de dados  
- [NumPy](https://numpy.org/) → Operações matemáticas  
- [Plotly](https://plotly.com/python/) → Gráficos interativos  
- [Jupyter Notebook](https://jupyter.org/) → Ambiente para análise  

---

## 📊 Estrutura da Base de Dados (`cancelamentos.csv`)

A base contém informações sobre clientes, como:

- **CustomerID** → Identificação do cliente (removida da análise por ser irrelevante).  
- **LigacoesCallCenter** → Quantidade de vezes que o cliente ligou para o suporte.  
- **DiasAtraso** → Quantidade de dias de atraso no pagamento.  
- **DuracaoContrato** → Tipo de contrato (Mensal, Anual, etc.).  
- **Cancelou** → Indica se o cliente cancelou (1) ou permaneceu (0).  

---

## 📈 Passos da Análise

1. **Importação da base de dados**  
   Carregamos a base `cancelamentos.csv` com o Pandas.  

2. **Limpeza dos dados**  
   - Remoção de colunas inúteis (`CustomerID`).  
   - Tratamento de valores nulos.  

3. **Análise inicial**  
   - Percentual de clientes que cancelaram vs. que permaneceram.  

4. **Investigação de causas**  
   - Clientes que ligaram **+4 vezes** ao call center → alto índice de cancelamento.  
   - Clientes com **+20 dias de atraso** → cancelaram quase sempre.  
   - Clientes com **contrato mensal** → maior risco de churn.  

5. **Ações sugeridas**  
   - Criar alerta quando cliente ligar **3 vezes** ao suporte.  
   - Criar alerta quando cliente atrasar **10 dias** no pagamento.  
   - Dar **desconto em contratos mais longos** para reduzir cancelamentos mensais.  

---

## ▶️ Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/projeto-cancelamentos.git
Instale as dependências:

bash
Copiar código
pip install pandas numpy plotly notebook
Abra o Jupyter Notebook:

bash
Copiar código
jupyter notebook inicial.ipynb
Execute as células em sequência para reproduzir a análise.

📊 Insights Obtidos
O atraso de pagamentos e a quantidade de contatos com o suporte são fatores críticos no cancelamento.

Alterando apenas 3 variáveis (atraso, call center e contrato), a taxa de cancelamento pode ser reduzida significativamente.
