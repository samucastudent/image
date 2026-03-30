# 🚀 Como Usar o GitHub Image Uploader

Script Python que automatiza o upload de imagens para o GitHub via API e já retorna os links **jsDelivr** prontos para uso.

---

## 📋 Pré-requisitos

- Python 3.6 ou superior instalado
- Conta no GitHub com um repositório público criado
- Conexão com a internet

---

## ⚙️ Instalação

Instale a única dependência necessária:

```bash
pip install requests
```

---

## 🔑 Gerar o Token do GitHub

1. Acesse: [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. Clique em **Generate new token (classic)**
3. Dê um nome ao token (ex: `image-uploader`)
4. Marque a permissão **`repo`** (acesso completo ao repositório)
5. Clique em **Generate token** e copie o valor gerado

> ⚠️ O token só aparece uma vez. Salve em lugar seguro!

---

## 🛠️ Configuração

Abra o arquivo `upload_github_imagens.py` e edite as variáveis no topo:

```python
GITHUB_TOKEN   = "SEU_TOKEN_AQUI"        # ← cole seu Personal Access Token
GITHUB_USER    = "samucastudent"          # ← seu usuário no GitHub
GITHUB_REPO    = "NOME_DO_REPOSITORIO"    # ← ex: "meus-imagens"
GITHUB_BRANCH  = "main"                   # ← branch padrão (main ou master)
PASTA_DESTINO  = "imagens"               # ← pasta de destino no repositório
PASTA_LOCAL    = "./imagens"              # ← pasta local com as imagens
```

---

## 🖼️ Preparar as Imagens

Crie uma pasta chamada `imagens/` no mesmo diretório do script e coloque suas imagens dentro:

📁 seu-projeto/
├── upload_github_imagens.py
└── 📁 imagens/
├── logo.png
├── banner.jpg
└── icone.webp

### Extensões aceitas

`.jpg` · `.jpeg` · `.png` · `.gif` · `.webp` · `.svg` · `.ico`

---

## ▶️ Executar

```bash
python upload_github_imagens.py
```

---

## 📤 Saída esperada

🚀 Iniciando upload de 3 imagem(ns) para 'samucastudent/meus-imagens/imagens'...

✅ Enviado: logo.png
🔗 jsDelivr: https://cdn.jsdelivr.net/gh/samucastudent/meus-imagens@main/imagens/logo.png

✅ Enviado: banner.jpg
🔗 jsDelivr: https://cdn.jsdelivr.net/gh/samucastudent/meus-imagens@main/imagens/banner.jpg

✅ Enviado: icone.webp
🔗 jsDelivr: https://cdn.jsdelivr.net/gh/samucastudent/meus-imagens@main/imagens/icone.webp

🎉 Processo concluído!
📦 Repositório: https://github.com/samucastudent/meus-imagens
🌐 CDN base: https://cdn.jsdelivr.net/gh/samucastudent/meus-imagens@main/imagens/


---

## 🌐 Usar as Imagens

Após o upload, use os links gerados diretamente em HTML ou Markdown:

**HTML:**
```html
<img src="https://cdn.jsdelivr.net/gh/samucastudent/meus-imagens@main/imagens/logo.png" alt="Logo">
```

**Markdown:**
```markdown

```

---

## 🔄 Atualizar uma imagem existente

Basta substituir o arquivo na pasta `imagens/` local e rodar o script novamente. Ele detecta automaticamente que o arquivo já existe e faz a atualização.

Para forçar o cache do jsDelivr a atualizar, adicione `?v=2` ao final da URL:

https://cdn.jsdelivr.net/gh/samucastudent/meus-imagens@main/imagens/logo.png?v=2


---

## 🔒 Segurança

Nunca suba o script com o token preenchido para o GitHub. Em vez disso, use variável de ambiente:

```python
import os
GITHUB_TOKEN = os.environ.get("GITHUB_TOKEN")
```

E defina no terminal antes de rodar:

```bash
# Linux / macOS
export GITHUB_TOKEN="ghp_xxxxxxxxxxxxxxxxxxxx"

# Windows (CMD)
set GITHUB_TOKEN=ghp_xxxxxxxxxxxxxxxxxxxx
```

---

## 📁 Estrutura do Repositório

Após o uso, seu repositório ficará assim:

📦 meus-imagens/
├── 📄 README.md
├── 📄 COMO_USAR.md
├── 🐍 upload_github_imagens.py
└── 📁 imagens/
├── logo.png
├── banner.jpg
└── icone.webp

---
## 🔙 Voltar

← **[Voltar ao README principal](README.md)**

Feito com ❤️ por [samucastudent](https://github.com/samucastudent)
