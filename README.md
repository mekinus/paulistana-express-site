# Paulistana Express Pizzaria — Site de Lançamento

Site institucional estático (HTML + CSS + JavaScript puro) para a inauguração da
**Paulistana Express Pizzaria** em Belém do Pará — Junho de 2026.

Sem backend, sem banco de dados, sem frameworks. Pronto para o **GitHub Pages**.

🌐 Domínio: **www.paulistanaexpresspizzaria.com.br**

---

## 📁 Estrutura do projeto

```
.
├── index.html              # Página única (hero, sobre, diferenciais, contagem, contato, redes, FAQ, footer)
├── CNAME                   # Domínio customizado do GitHub Pages
├── .nojekyll               # Desativa o processamento Jekyll do GitHub Pages
├── robots.txt              # Diretrizes para buscadores
├── sitemap.xml             # Mapa do site para SEO
└── assets/
    ├── css/
    │   ├── tokens.css      # Tokens da marca (cores, tipografia, espaçamento)
    │   └── styles.css      # Estilos do site
    ├── js/
    │   └── main.js         # Contagem regressiva, menu, FAQ, animações de scroll
    ├── fonts/
    │   └── Lobster-Regular.ttf
    └── images/
        ├── logo.jpg        # Logo principal
        ├── favicon.png
        └── og-image.jpg    # Imagem de compartilhamento (Open Graph / Twitter)
```

---

## 🚀 Deploy no GitHub Pages — passo a passo

### 1. Criar o repositório e enviar os arquivos

```bash
# Na raiz do projeto
git init
git add .
git commit -m "Site de lançamento Paulistana Express Pizzaria"
git branch -M main

# Criar o repositório no GitHub (via GitHub CLI)
gh repo create paulistana-express-site --public --source=. --remote=origin --push

# OU, se o repositório já existe:
# git remote add origin https://github.com/SEU_USUARIO/paulistana-express-site.git
# git push -u origin main
```

### 2. Ativar o GitHub Pages

No GitHub: **Settings → Pages**
- **Source:** `Deploy from a branch`
- **Branch:** `main` / `/ (root)`
- Salvar.

Em 1–2 minutos o site estará no ar em `https://SEU_USUARIO.github.io/paulistana-express-site/`.

### 3. Configurar o domínio customizado

O arquivo **`CNAME`** já está incluído com `www.paulistanaexpresspizzaria.com.br`.

No GitHub: **Settings → Pages → Custom domain** já deve aparecer preenchido.
Marque **Enforce HTTPS** após a validação do certificado.

### 4. Configurar o DNS (no provedor do domínio)

| Tipo  | Nome (host) | Valor |
|-------|-------------|-------|
| CNAME | `www`       | `SEU_USUARIO.github.io` |
| A     | `@`         | `185.199.108.153` |
| A     | `@`         | `185.199.109.153` |
| A     | `@`         | `185.199.110.153` |
| A     | `@`         | `185.199.111.153` |

> Os 4 registros `A` no domínio raiz (`@`) garantem que
> `paulistanaexpresspizzaria.com.br` redirecione para a versão `www`.
> A propagação do DNS pode levar de minutos a algumas horas.

---

## ✏️ Como atualizar o conteúdo

- **Data da inauguração / contagem regressiva:** `assets/js/main.js` → constante `TARGET`.
- **Telefone WhatsApp:** procure por `5591991542323` (links) e `91 99154-2323` (texto exibido).
- **Instagram:** procure por `paulistanafoodexpress`.
- **Endereço:** procure por `Rodovia Mário Covas`.
- **Foto da seção "Sobre":** substitua o placeholder em `index.html` (`.imgslot`)
  por uma `<img>` apontando para um arquivo em `assets/images/`.
- **Facebook / TikTok:** atualize os `href="#"` quando os links existirem.
- **Cores e tipografia:** `assets/css/tokens.css`.

Após editar, basta um novo commit + push — o GitHub Pages atualiza automaticamente.

---

## 🔍 SEO já incluído

- Meta title + description otimizados para "pizzaria em Belém", "pizza delivery Belém".
- Open Graph + Twitter Cards (com `og-image.jpg`).
- Structured Data (JSON-LD) do tipo `Restaurant` / Local Business.
- `robots.txt` + `sitemap.xml`.

> Lembre de enviar o `sitemap.xml` no **Google Search Console** após o deploy.

---

© 2026 Paulistana Express Pizzaria. Todos os direitos reservados.
