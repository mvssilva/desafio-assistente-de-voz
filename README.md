# Assistente de Voz Inteligente com RAG

Este projeto apresenta um assistente de voz avançado capaz de consultar documentos PDF específicos para responder perguntas via áudio, utilizando a arquitetura **RAG (Retrieval-Augmented Generation)**.

## Funcionalidades
- **Interface de Voz:** Captura de áudio no navegador via JavaScript no Google Colab.
- **Transcrição:** Uso do modelo **OpenAI Whisper (small)**.
- **Cérebro (LLM):** Processamento de contexto com **Google Gemini 1.5 Flash**.
- **Memória Semântica:** Busca de trechos relevantes em PDF utilizando **ChromaDB** e **LangChain**.
- **Síntese de Voz:** Respostas convertidas em áudio com **gTTS**.

## Tecnologias Utilizadas
- **Python**
- **LangChain** (Orquestração)
- **Google Gemini API** (LLM & Embeddings)
- **OpenAI Whisper** (STT)
- **ChromaDB** (Banco de Vetores)
- **gTTS** (TTS)

## Arquitetura do Projeto

1. **Ingestão:** O PDF é carregado, fatiado em blocos e transformado em vetores.
2. **Pergunta:** O áudio do usuário é gravado e transcrito para texto.
3. **Busca:** O sistema localiza no PDF os trechos mais relevantes à pergunta.
4. **Geração:** O Gemini formula a resposta baseada no contexto do documento.
5. **Saída:** A resposta é convertida em áudio e reproduzida.

## Como Executar
1. Configure a sua chave de API nos "Secrets" do Google Colab como `KEY_API_GEMINI`.
2. Certifique-se de que o PDF está no caminho correto indicado no código.
3. Execute as células do notebook em ordem.

---
**Desenvolvido por Marcos Silva** 
