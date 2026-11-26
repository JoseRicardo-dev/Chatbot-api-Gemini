# 🤖 Chatbot Conversacional com Google Gemini API

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JoseRicardo-dev/Chatbot-api-Gemini/blob/main/Chat_bot_Gemini_API.ipynb)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google%20Gemini%20API-1.5%20Flash-8E75B2?logo=google&logoColor=white)
![Streamlit](https://img.shields.io/badge/Interface-Streamlit-FF4B4B?logo=streamlit&logoColor=white)

Assistente conversacional interativo desenvolvido em Python utilizando o SDK oficial do Google Generative AI (`google-generativeai`). O projeto oferece três modos de execução: **Interface Web (Streamlit)**, **Linha de Comando (CLI)** e **Google Colab**, mantendo o histórico e o contexto da conversa em tempo real.

---

## 🎯 Destaques Técnicos

* **Gerenciamento de Contexto (Stateful Chat):** Uso de `start_chat(history=[])` aliado ao gerenciamento de estado (`st.session_state` na interface web) para preservar a memória da conversa entre turnos.
* **Arquitetura Multi-Ambiente:** Código modularizado para rodar tanto na nuvem (Google Colab) quanto localmente via terminal ou navegador web.
* **Segurança de Credenciais:** Isolamento completo de chaves de API utilizando variáveis de ambiente (`.env` com `python-dotenv`), `.gitignore` configurado e `userdata` no Colab.
* **Engenharia de Prompt (System Instructions):** Configuração de instruções de sistema na inicialização do modelo para guiar o comportamento e o tom das respostas.
* **Tratamento de Exceções:** Validação de credenciais e tratamento de falhas de rede/API para evitar interrupções inesperadas.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3.10+
* **IA Generativa:** `google-generativeai` (Modelo `gemini-1.5-flash-latest`)
* **Front-end Web:** `streamlit`
* **Gerenciamento de Ambiente:** `python-dotenv`
* **Prototipação:** Google Colaboratory (Jupyter Notebook)

---

## 📂 Estrutura do Repositório

```text
Chatbot-api-Gemini/
├── app.py                      # Aplicação Web interativa com Streamlit
├── cli_chat.py                 # Versão de linha de comando (Terminal)
├── Chat_bot_Gemini_API.ipynb   # Notebook original para execução no Google Colab
├── requirements.txt            # Dependências do projeto
├── .env.example                # Modelo de configuração de variáveis de ambiente
├── .gitignore                  # Arquivos ignorados pelo Git (proteção de segredos)
└── README.md                   # Documentação do projeto
```

---

## 🚀 Como Executar o Projeto

### Opção 1: Execução Local (Interface Web ou Terminal)

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/JoseRicardo-dev/Chatbot-api-Gemini.git
   cd Chatbot-api-Gemini
   ```

2. **Crie e ative um ambiente virtual:**
   ```bash
   python -m venv venv
   # No Windows:
   venv\Scripts\activate
   # No Linux/macOS:
   source venv/bin/activate
   ```

3. **Instale as dependências:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure sua chave de API:**
   * Gere uma chave gratuita no [Google AI Studio](https://aistudio.google.com/).
   * Renomeie o arquivo `.env.example` para `.env` e adicione sua chave:
     ```env
     GOOGLE_GEMINI_API_KEY=sua_chave_aqui
     ```

5. **Execute a aplicação:**
   * **Para abrir a Interface Web (Streamlit):**
     ```bash
     streamlit run app.py
     ```
   * **Para rodar no Terminal (CLI):**
     ```bash
     python cli_chat.py
     ```

---

### Opção 2: Execução na Nuvem (Google Colab)

1. Clique no botão **"Open in Colab"** no topo deste documento.
2. No menu lateral esquerdo do Colab, acesse **Secrets (ícone de chave)**, crie a variável `GOOGLE_GEMINI_API_KEY` com sua chave e habilite o acesso ao notebook.
3. Execute todas as células (`Ctrl + F9`) e digite `fim` quando quiser encerrar o chat.

---

## 👨‍💻 Autor

Desenvolvido por **José Ricardo**  
[![GitHub](https://img.shields.io/badge/GitHub-JoseRicardo--dev-181717?logo=github)](https://github.com/JoseRicardo-dev)

