# Microsoft Translator API - Documentação Python

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Microsoft Translator](https://img.shields.io/badge/API-Microsoft%20Translator-orange.svg)](https://azure.microsoft.com/en-us/services/cognitive-services/translator/)

Este projeto demonstra a integração com APIs de tradução através de dois scripts Python que implementam tradução automática de documentos e páginas web. Desenvolvido para o **Microsoft Certification Challenge #4 - AI 102**.

## Visão Geral

A documentação apresenta dois scripts Python essenciais para tradução de conteúdo usando APIs de tradução:

- **DOCX Translator**: Tradução de documentos Word preservando formatação
- **Webpage Translator**: Tradução de páginas web com limpeza e exportação HTML

Os scripts demonstram preservação de formatação e estrutura durante o processo de tradução automática.

## Funcionalidades

### DOCX Translator

- Configuração via PROVIDER_KEY para API de tradução
- Tradução de documentos Word preservando formatação
- Manutenção de títulos, parágrafos, listas e ênfases
- Suporte a múltiplos idiomas
- Tratamento robusto de erros

### Webpage Translator

- Download de páginas web via URL
- Limpeza de scripts e estilos CSS
- Extração de texto limpo preservando estrutura HTML
- Tradução do conteúdo para idioma escolhido
- Exportação de HTML traduzido

## Pré-requisitos

- Python 3.7 ou superior
- Bibliotecas: `requests`, `python-docx`, `beautifulsoup4`, `lxml`
- Chave de API de tradução (PROVIDER_KEY)
- Conexão com internet para acessar a API

## Instalação

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/microsoft-translator-api.git
cd microsoft-translator-api
```

### 2. Crie um ambiente virtual

```bash
# Criar ambiente virtual
python3 -m venv venv

# Ativar ambiente virtual
# No Windows:
venv\Scripts\activate
# No macOS/Linux:
source venv/bin/activate
```

### 3. Instale as dependências

```bash
pip install requests python-docx beautifulsoup4 lxml
```

### 4. Configure sua chave de API

Edite os arquivos `docx-translator.py` e `webpage-translator.py` e substitua `"SUA_CHAVE_DE_API_AQUI"` pela sua chave de API de tradução.

## Como Usar

### DOCX Translator

```bash
python3 docx-translator.py
```

**Exemplo de saída:**

```
Arquivo original: documento.docx
Arquivo traduzido: documento_pt.docx
Formatação preservada: Sim
Estrutura mantida: Títulos, parágrafos, negrito, itálico
```

### Webpage Translator

```bash
python3 webpage-translator.py
```

**Exemplo de saída:**

```
URL Original: https://example.com/page
HTML traduzido: <html><body><h1>Título Traduzido</h1><p>Conteúdo traduzido...</p></body></html>
Arquivo salvo: example_com_page_pt.html
```

## Estrutura do Projeto

```
projeto/
├── docx-translator.py   # Tradução de Documentos DOCX
├── webpage-translator.py # Tradução de Páginas Web
├── index.html           # Documentação completa
├── projetos.md          # Documentação dos projetos
├── venv/                # Ambiente virtual
├── .env                 # Variáveis de ambiente (opcional)
└── README.md            # Este arquivo
```

## Configuração da API

### 1. Obtenha sua chave de API

1. Acesse o [Azure Portal](https://portal.azure.com) ou outro provedor de tradução
2. Crie um recurso de tradução nos Cognitive Services
3. Copie a chave de API

### 2. Configure as variáveis

```python
PROVIDER_KEY = "SUA_CHAVE_DE_API_AQUI"
target_language = "pt-br"  # Idioma de destino
```

## Documentação Completa

Para visualizar a documentação completa com exemplos interativos, abra o arquivo `index.html` em seu navegador.

A documentação inclui:

- Explicações passo-a-passo
- Exemplos de código comentados
- Demonstrações interativas
- Guia de configuração
- Referência da API

## Exemplos de Uso

### DOCX Translator

```python
# Traduzir documento DOCX preservando formatação
from docx_translator import translate_document

# Traduzir arquivo DOCX
translate_document("documento.docx", "pt-br")
# Resultado: documento_pt.docx com formatação preservada
```

### Webpage Translator

```python
# Traduzir página web e exportar HTML
from webpage_translator import translate_webpage

# Traduzir página web
translate_webpage("https://example.com", "pt-br")
# Resultado: example_com_pt.html com conteúdo traduzido
```

## Diferenças Entre os Projetos

| Característica | DOCX Translator             | Webpage Translator     |
| -------------- | --------------------------- | ---------------------- |
| Foco           | Documentos Word             | Páginas web            |
| Formatação     | Preserva DOCX               | Preserva HTML          |
| Limpeza        | Não necessária              | Remove scripts/styles  |
| Saída          | Arquivo DOCX traduzido      | Arquivo HTML traduzido |
| Estrutura      | Títulos, parágrafos, listas | Estrutura HTML básica  |
| Configuração   | PROVIDER_KEY                | PROVIDER_KEY           |

## Tratamento de Erros

Os scripts incluem tratamento para:

- Validação de chave de API e configurações
- Verificação de conectividade com a API
- Tratamento de erros de resposta HTTP
- Validação de formato de entrada (DOCX/URL)
- Mensagens de erro claras e informativas
- Preservação de formatação durante tradução

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

## Autor

**Esly Barbosa**

- Microsoft Certification Challenge #4 - AI 102
- Desenvolvido para fins educacionais

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para:

1. Fazer um fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abrir um Pull Request

## Suporte

Se você encontrar algum problema ou tiver dúvidas:

1. Verifique a [documentação completa](index.html)
2. Abra uma [issue](https://github.com/seu-usuario/microsoft-translator-api/issues)
3. Consulte a [documentação oficial da Microsoft Translator API](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/)

## Links Úteis

- [Microsoft Translator API Documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/)
- [Azure Cognitive Services](https://azure.microsoft.com/en-us/services/cognitive-services/)
- [Python Requests Library](https://docs.python-requests.org/)
- [python-docx Documentation](https://python-docx.readthedocs.io/)
- [BeautifulSoup4 Documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)

---

**Se este projeto foi útil para você, considere dar uma estrela!**
