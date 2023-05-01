## Overview

#### Docs
[LangChain Documentation](https://python.langchain.com/en/latest/index.html)

#### What is LangChain?
From [LangChain](https://python.langchain.com/en/latest/index.html): LangChain is a framework for developing applications powered by language models. From [Pinecone](https://www.pinecone.io/learn/langchain-intro/): At its core, LangChain is a framework built around LLMs. LangChain is used for chatbots, Generative Question-Answering (GQA), summarization, and much more.

The core idea of the library is that you can “chain” together different components to create more advanced use cases around LLMs. Chains may consist of multiple components from several modules:

1. Prompt templates: Prompt templates are templates for different types of prompts. Like “chatbot” style templates, ELI5 question-answering, etc
2. LLMs: Large language models like GPT-3, BLOOM, etc
3. Agents: Agents use LLMs to decide what actions should be taken. Tools like web search or calculators can be used, and all are packaged into a logical loop of operations.
4. Memory: Short-term memory, long-term memory.