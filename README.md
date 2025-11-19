[README.md](https://github.com/user-attachments/files/23639143/README.md)
# Atividade-11-Indo-Al-m-Hugging-Face-

# 🤖 RAG Chatbot com Hugging Face

Este repositório contém uma implementação simples de um sistema **RAG (Retrieval Augmented Generation)** desenvolvido em Python. O projeto demonstra como combinar busca semântica com Modelos de Linguagem (LLMs) para criar respostas baseadas em contexto específico.

## 📋 Sobre o Projeto

O objetivo deste projeto é resolver o problema de alucinação das IAs e a falta de conhecimento sobre dados privados. Utilizamos uma base de conhecimento vetorial para fornecer contexto ao modelo antes que ele gere uma resposta.

### 🛠 Tecnologias Utilizadas

* **Python**: Linguagem principal.
* **Hugging Face Transformers**: Para carregar os modelos de IA.
* **Sentence-Transformers**: Para converter texto em embeddings (vetores numéricos).
* **FAISS (Facebook AI Similarity Search)**: Para indexação e busca rápida de vetores.
* **Google Flan-T5**: LLM utilizado para gerar as respostas finais.

## 🚀 Como Funciona

O fluxo da aplicação segue os passos abaixo:

1.  **Indexação**: Documentos de texto são convertidos em vetores numéricos (*embeddings*) e armazenados no índice FAISS.
2.  **Recuperação (Retrieval)**: Quando o usuário faz uma pergunta, o sistema busca o trecho de texto mais similar na base de dados.
3.  **Geração (Generation)**: O texto recuperado e a pergunta são enviados para o modelo Flan-T5, que gera uma resposta natural.

## 📂 Estrutura do Repositório

* `atividade_rag_huggingface.ipynb`: O código fonte completo (Notebook) pronto para execução no Google Colab ou Jupyter.
* `apresentacao_rag.pdf`: Slides explicativos sobre o problema, a solução e a arquitetura utilizada.

## 💻 Como Executar

1.  Baixe o arquivo `.ipynb`.
2.  Abra no [Google Colab](https://colab.research.google.com/) ou Jupyter Notebook.
3.  Instale as dependências na primeira célula:
    ```python
    !pip install transformers sentence-transformers faiss-cpu
    ```
4.  Execute as células sequencialmente para ver o RAG em ação.

---
*Desenvolvido como atividade acadêmica sobre LLMs e Vector Databases.*
