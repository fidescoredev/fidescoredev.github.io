# Fides Core Dev — Site (GitHub Pages)

Site estático bilíngue (PT/EN) da **Fides Core Dev**, com paleta roxo/dourado, favicon e metatags Open Graph.

## Estrutura
```
index.html
politica-de-privacidade.html
Fides_Core_logo_corporativo_roxo_dourado_premium.png
favicon.ico
favicon-16x16.png
favicon-32x32.png
favicon-48x48.png
favicon-64x64.png
favicon-192x192.png
favicon-512x512.png
apple-touch-icon.png
og-image-fides.png
.nojekyll
```
> O arquivo `.nojekyll` impede o processamento do Jekyll no GitHub Pages.

## Publicação rápida

### 1) Repositório de **usuário** (raiz do domínio)
Use **`<SEU_USUARIO>.github.io`** como nome do repo.
URL final: `https://<SEU_USUARIO>.github.io/`

```bash
# Dentro da pasta com os arquivos do site
git init
git add .
git commit -m "Publica site Fides Core Dev"
git branch -M main
git remote add origin https://github.com/<SEU_USUARIO>/<SEU_USUARIO>.github.io.git
git push -u origin main
```

Ative o Pages em **Settings > Pages** → *Deploy from a branch* → `main` / root.

### 2) Repositório de **projeto**
Nomeie como quiser (ex.: `fidescoredev-site`).
URL final: `https://<SEU_USUARIO>.github.io/<REPO>/`

```bash
git init
git add .
git commit -m "Publica site Fides Core Dev"
git branch -M main
git remote add origin https://github.com/<SEU_USUARIO>/<REPO>.git
git push -u origin main
```

Ative o Pages em **Settings > Pages** → *Deploy from a branch* → `main` / root.

> Se optar por repositório de projeto, mantenha links **relativos** (já estão corretos).

## Domínio personalizado (opcional)

1. Em **Settings > Pages**, defina seu domínio (cria o arquivo `CNAME` automat.), **ou** crie você mesmo um arquivo `CNAME` na raiz contendo apenas:
```
seu-dominio.com
```
2. No DNS:
   - `www` → CNAME para `<SEU_USUARIO>.github.io`
   - raiz (apex) → A records dos IPs do GitHub Pages (ou ALIAS/ANAME se suportado).
3. Ative **Enforce HTTPS** após emitir o certificado.
4. Troque as metas `og:image` por URL absoluta, ex.:
```html
<meta property="og:image" content="https://seu-dominio.com/og-image-fides.png">
<meta name="twitter:image" content="https://seu-dominio.com/og-image-fides.png">
```

## Atualizações
Faça alterações, commite e `git push`. O Pages redeploya automaticamente (ver **Deployments**).

## Licença
Defina a licença que preferir (MIT/Apache-2.0/etc.) se for abrir o código.
