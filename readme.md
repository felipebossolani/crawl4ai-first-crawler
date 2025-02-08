# Projeto: Web Scraping com Crawl4AI

Este projeto utiliza a biblioteca [Crawl4AI](https://github.com/unclecode/crawl4ai) para realizar scraping de sites de forma assíncrona. O código busca informações da página de notícias da NBC e retorna o conteúdo formatado em Markdown.

## 📌 Tecnologias Utilizadas
- **Python 3.8+**
- **Crawl4AI** (para scraping)
- **Asyncio** (para execução assíncrona)

## 🚀 Instalação e Configuração
Para rodar este projeto localmente, siga os passos abaixo:

### 1️⃣ **Clone o repositório**
```sh
 git clone https://github.com/felipebossolani/crawl4ai-first-crawler.git
 cd crawl4ai-first-crawler
```

### 2️⃣ **Crie um ambiente virtual (opcional, mas recomendado)**
```sh
python3 -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate    # Windows
```

### 3️⃣ **Instale as dependências**
```sh
pip install crawl4ai
```

## 📝 Como Usar
Execute o script para rodar o crawler:

```sh
python main.py
```

### 📜 Código Principal (`main.py`)
```python
import asyncio
from crawl4ai import *

async def main():
    async with AsyncWebCrawler() as crawler:
        result = await crawler.arun(
            url="https://www.nbcnews.com/business",
        )
        print(result.markdown)

if __name__ == "__main__":
    asyncio.run(main())
```

## ℹ️ Sobre a Biblioteca Crawl4AI
[Crawl4AI](https://github.com/unclecode/crawl4ai) é uma biblioteca Python para web scraping assíncrono, ideal para extração de dados de páginas da web de maneira eficiente. Suporta integração com inteligência artificial para extração avançada de informações.

## 📌 Próximos Passos
- Melhorar o tratamento dos dados extraídos
- Adicionar suporte a múltiplas URLs
- Explorar funcionalidades avançadas do Crawl4AI

---
Criado por [Felipe Bossolani](https://github.com/felipebossolani).

