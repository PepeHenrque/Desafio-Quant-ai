# 🏛️ Robô Janus: Quant AI & ESG Strategy

> **🏆 Projeto classificado no Top 15 Brasil - Desafio QuantIA 2025**

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![AI Model](https://img.shields.io/badge/LLM-Google%20Gemini%202.5%20Flash-orange)](https://ai.google.dev/)
[![Status](https://img.shields.io/badge/Status-Finalizado-success)]()

O **Janus** é um algoritmo de trading quantitativo desenvolvido para testar a hipótese do **"Alpha Sustentável"**. Ele combina o rigor estatístico do **Estudo de Eventos** com a capacidade interpretativa da **Inteligência Artificial Generativa** para operar janelas de oportunidade baseadas em notícias ESG (Ambiental, Social e Governança) no mercado brasileiro (B3).

---

## 📖 Sobre o Projeto

Inspirado no deus romano de duas faces, o **Janus** possui uma abordagem dual:
1.  **Face Analista (Passado):** Varre dados históricos e utiliza IA para classificar semanticamente notícias, filtrando ruídos.
2.  **Face Estrategista (Futuro):** Aplica regras quantitativas objetivas para gerenciar posições e buscar Alpha.

### 🎯 A Tese de Investimento
Acreditamos na existência de uma assimetria informacional: o mercado reage instantaneamente a dados financeiros, mas **sub-reage** (é lento) ao incorporar o valor de longo prazo de eventos ESG positivos, criando uma janela tática de valorização nos dias subsequentes ao evento.

---

## 🛠️ Tech Stack e Arquitetura

O projeto foi construído em Python, integrando APIs financeiras e Modelos de Linguagem (LLMs).

* **Core:** `Python`, `Pandas`, `NumPy`.
* **AI Engine:** `Google Gemini API` (Modelo: `gemini-2.5-flash-lite`).
* **Data Sources:**
    * Notícias: `GNews` (Scraping estruturado).
    * Preços: `YFinance` (Dados diários ajustados da B3).
* **Visualização:** `Matplotlib`.

*(Fluxo: Coleta GNews -> Classificação Gemini -> Estudo de Eventos -> Backtest)* 

---

## 🧠 Metodologia Científica

Diferente de backtests simples, utilizamos a metodologia de **Event Study** (MacKinlay, 1997) para isolar o retorno anormal (Alpha).

### 1. Universo de Ativos
Focamos em empresas líderes ou com alta visibilidade na pauta de transição energética:
* `PETR4` (Petrobras)
* `VALE3` (Vale)
* `SUZB3` (Suzano)
* `AMBP3` (Ambipar)
* `ELET3` (Eletrobras)
* `RAIZ4` (Raízen)

### 2. Classificação via GenAI (O Diferencial)
Em vez de simples palavras-chave, usamos o **Google Gemini** para ler as manchetes e responder a um prompt rigoroso: *"A manchete reporta um novo e concreto investimento ou iniciativa positiva?"*.
* **Total de Eventos Identificados:** 203 eventos qualificados entre 2015 e 2024.

### 3. Validação Robusta (Train vs. Test)
Para evitar o *Overfitting* (vício de otimização), dividimos os dados rigidamente:
* **In-Sample (Treino):** 2015 - 2021
* **Out-of-Sample (Teste):** 2022 - 2024

---

## 📊 Resultados e Descobertas

O projeto gerou insights valiosos sobre a eficiência do mercado e a armadilha do overfitting.

### Fase de Treino (A Descoberta da Regra)
Nos dados de treino, identificamos um padrão promissor:
* **Pico de Alfa:** +5,49% acima do Ibovespa.
* **Janela Ideal:** Ocorria no **12º dia útil (D+12)** após a notícia.

### Fase de Teste
Ao aplicar a regra de "Venda no D+12" nos dados de teste (2022-2024), o padrão não se sustentou, resultando em um Alfa próximo de zero (-0,27%).

### 💡 Conclusão do Estudo
O Janus foi um sucesso metodológico. Ele provou que:
1.  **A IA funciona:** O Gemini foi capaz de filtrar e classificar eventos complexos.
2.  **O Rigor Salva:** A separação *Out-of-Sample* protegeu contra uma estratégia que parecia lucrativa no papel, mas era um artefato estatístico do passado.
3.  **Hipótese Validada:** O mercado atual precifica notícias ESG de forma mais eficiente ou ruidosa do que no passado, exigindo análises que vão além da manchete (ex: análise do corpo da notícia com NLP avançado).


---
**Autores:** Weslley Silva, Rosimere Alcântara e Pedro Henrique, Equipe Capibit³.
*Projeto desenvolvido para o Desafio Quant AI 2025.*
