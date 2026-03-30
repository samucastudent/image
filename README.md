# 🖼️ Tutorial: Usar o GitHub como hospedagem de imagens com jsDelivr

Aprenda a usar o **GitHub** como *host* de imagens e acessar essas imagens diretamente via **jsDelivr**, para usar em sites, READMEs ou qualquer outro lugar na web. 🚀

---

## 1. 🛠️ Criar o repositório no GitHub

1. Acesse [https://github.com](https://github.com) e faça login. 🔐  
2. Clique em **New** (ou **New repository**). ➕  
3. Preencha:
   - **Repository name**: por exemplo, `meus-imagens` 📂  
   - **Public** (importante, repositórios privados não funcionam bem com jsDelivr). 🔓  
4. Marque **Add a README file** (opcional, mas recomendado). ✅  
5. Clique em **Create repository**. 🎉

---

## 2. 🖼️ Subir imagens para o repositório

### 2.1. Via interface web 🖱️

1. Entre no repositório (ex: `seu-usuario/meus-imagens`).  
2. Clique em **Add file** → **Upload files**. 📤  
3. Arraste ou selecione as imagens (`.jpg`, `.png`, `.webp`, etc.). 📷  
4. Clique em **Commit changes**. ✅

### 2.2. Via Git (linha de comando) 💻

```bash
git clone https://github.com/seu-usuario/meus-imagens.git
cd meus-imagens

# Copie imagens para a pasta (ex: imagens/)
mkdir -p imagens
cp ~/Downloads/foto.jpg imagens/

git add .
git commit -m "Adiciona imagem foto.jpg" 🎨
git push origin main 🚀
```

---

## 3. 🔗 Obter o link direto do GitHub (opcional)

1. Acesse o repositório no GitHub. 👀  
2. Abra a pasta onde estão as imagens. 📂  
3. Clique com o botão direito na imagem → **Open link in new tab**. 🔗  
4. A URL será algo como:
   ```text
   https://github.com/seu-usuario/meus-imagens/blob/main/imagens/foto.jpg
   ```
   Para usar a imagem em algum lugar, troque `blob` por `raw`:
   ```text
   https://github.com/seu-usuario/meus-imagens/raw/main/imagens/foto.jpg
   ```

---

## 4. 🚀 Usar a imagem via jsDelivr (recomendado)

Com o jsDelivr, você pode servir as imagens com cache global e boa performance. ⚡

### 4.1. Formato da URL do jsDelivr 📜

Use esse padrão:

```text
https://cdn.jsdelivr.net/gh/usuario/repositorio@branch/caminho/para/imagem.jpg
```

- `usuario`: seu nome de usuário no GitHub. 👤  
- `repositorio`: o nome do repositório (ex: `meus-imagens`). 📦  
- `branch`: normalmente `main` ou `master`. 🌿  
- `caminho/para/imagem.jpg`: caminho dentro do repositório. 📂

Exemplo:

```text
https://cdn.jsdelivr.net/gh/samuel/meus-imagens@main/imagens/foto.jpg
```

### 4.2. Usando no HTML 🖼️

```html
<img src="https://cdn.jsdelivr.net/gh/samuel/meus-imagens@main/imagens/foto.jpg"
     alt="Minha foto">
```

### 4.3. Usando no README.md do GitHub 📘

```markdown

```

---

## 5. 🔄 Atualizar imagens

1. Atualize o arquivo no repositório (mudança, novo upload, etc.). 🖌️  
2. Faça commit e push:
   ```bash
   git add .
   git commit -m "Atualiza foto.jpg" 🎨
   git push origin main 🚀
   ```
3. Peça ao jsDelivr para recriar o cache, adicionando um query param (opcional, na maioria dos casos não é necessário esperar algum tempo):
   ```text
   https://cdn.jsdelivr.net/gh/samuel/meus-imagens@main/imagens/foto.jpg?v=2
   ```

---

## 6. 💡 Dicas rápidas

- Use nomes simples: `logo.png`, `banner-home.jpg`, etc. 🧩  
- Evite caracteres especiais e espaços (use `traco` ou `underline`). 🔤  
- Prefira imagens otimizadas (webp/jpg) para melhor performance. 🖼️⚡  
- O jsDelivr é **gratuito** para uso público e não precisa de cadastro. 🎁

---

## 7. 📝 Exemplo de README completo para repositório de imagens

Crie um arquivo `README.md` na raiz do repositório:

```markdown
# Imagens publicadas 🖼️

Acesse as imagens diretamente via jsDelivr:

- [Logo](https://cdn.jsdelivr.net/gh/samuel/meus-imagens@main/imagens/logo.png)
- [Banner](https://cdn.jsdelivr.net/gh/samuel/meus-imagens@main/imagens/banner.jpg)
```

---

Pronto! Agora você tem um repositório GitHub funcionando como **host de imagens** e pode servir as imagens em qualquer site usando **jsDelivr**. 🎉✨

## 📚 Documentação

Para usar o script de upload automático:

🚀 **[Como Usar o GitHub Image Uploader](COMO_USAR.md)**

---

## 🖼️ Suas Imagens

Acesse suas imagens via jsDelivr:

- ![Logo](https://cdn.jsdelivr.net/gh/samucastudent/meus-imagens@main/imagens/logo.png)
- ![Banner](https://cdn.jsdelivr.net/gh/samucastudent/meus-imagens@main/imagens/banner.jpg)
