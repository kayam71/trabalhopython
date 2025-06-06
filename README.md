
# 📈 trabalhopython – Aplicativo de Análise de Ações com Yahoo Finance

Este projeto tem como objetivo criar um aplicativo Python que permite a análise gráfica de ações com dados históricos obtidos automaticamente da API do Yahoo Finance.

---

## 🧩 Componentes do Projeto

- **Usuário**: quem usará o aplicativo com interface gráfica.
- **Aplicativo**: desenvolvido em Python com interface gráfica (Tkinter, PyQt ou Flet).
- **G2_Mercado.DB**: banco de dados SQLite contendo os dados históricos de ações.
- **Yahoo Finance**: fonte dos dados históricos (últimos 360 dias).
- **Acoes.txt**: lista de tickers (um por linha) que devem ter seus dados carregados.
- **NaoCarregadas.txt**: lista dos tickers que falharam na busca.
- **Script Python**: lê o `Acoes.txt`, busca dados via Yahoo Finance e grava no banco `G2_Mercado.DB`.

---

## ⚙️ Funcionalidades

✅ Baixar dados históricos (abertura, fechamento, mínimo, máximo, volume) das ações listadas em `Acoes.txt`.  
✅ Armazenar os dados no banco `G2_Mercado.DB`.  
✅ Registrar falhas em `NaoCarregadas.txt`.  
✅ Exibir gráficos interativos (ex: candlestick) com base nas ações e datas escolhidas pelo usuário via interface gráfica.

---

## 🧪 Tecnologias Utilizadas

- Python 3.x  
- [yfinance](https://pypi.org/project/yfinance/)  
- pandas  
- plotly  
- sqlite3 (embutido no Python)  
- tkinter / pyqt5 / flet (à escolha)

---

## 📦 Instalação

Clone o repositório e instale os pacotes necessários:

```bash
git clone https://github.com/kayam71/trabalhopython.git
cd trabalhopython
pip install -r requirements.txt
```

---

## ▶️ Execução

1. Edite o arquivo `Acoes.txt` e adicione os tickers desejados, um por linha.
2. Execute o script para carregar os dados no banco:

```bash
python ScriptCarregamento.py
```

3. Execute o app gráfico:

```bash
python app.py
```

---

## 🗃️ Estrutura esperada no Banco de Dados

```sql
CREATE TABLE IF NOT EXISTS Acao (
    Ticker TEXT,
    Data TEXT,
    Abertura REAL,
    Fechamento REAL,
    Maximo REAL,
    Minimo REAL,
    Volume INTEGER
);
```

---

## 📁 Estrutura do Projeto

```
trabalhopython/
├── ScriptCarregamento.py
├── app.py
├── G2_Mercado.DB
├── Acoes.txt
├── NaoCarregadas.txt
├── requirements.txt
└── README.md
```

---

## 🧑‍💻 Autor

Kayam – Repositório criado para o desenvolvimento do trabalho acadêmico de programação com foco em análise de dados de mercado.
