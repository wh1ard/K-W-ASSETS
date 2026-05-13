# 🖼️ kw-assets — Repositório de Mídia (K&W Studio Bot)

Repositório **público e separado** para hospedar imagens e GIFs usados pelo bot.
As URLs `raw.githubusercontent.com` são servidas diretamente pelo GitHub — sem custo, sem CDN externo.

## 📁 Estrutura

```
kw-assets/
└── assets/
    ├── boas-vindas.gif      ← GIF de boas-vindas (embed de entrada de membro)
    ├── logo.png             ← Logo do servidor (thumbnail de embeds)
    └── velociraptor.png     ← Imagem do comando /velociraptor
```

## 🔗 Como usar as URLs

Após fazer upload dos arquivos neste repositório, as URLs seguem o padrão:

```
https://raw.githubusercontent.com/wh1ard/kw-assets/main/assets/ARQUIVO.ext
```

Configure essas URLs nas variáveis de ambiente do bot (SquareCloud ou `.env`):

| Variável         | Arquivo esperado           |
|------------------|----------------------------|
| `URL_GIF_BEM_VINDO` | `assets/boas-vindas.gif` |
| `URL_LOGO`          | `assets/logo.png`        |
| `URL_VELOCIRAPTOR`  | `assets/velociraptor.png`|

## ⚠️ Regras

- ✅ Este repositório deve ser **público** (o Discord precisa acessar as URLs diretamente)
- ✅ Arquivos aceitos: `.gif`, `.png`, `.jpg`, `.webp`
- ❌ **Nunca** coloque arquivos `.env`, tokens ou dados do servidor aqui
- ❌ Não hospede arquivos grandes (>50 MB) — use o GitHub LFS se necessário

## 🚀 Fazendo upload

```bash
# Clone este repositório
git clone https://github.com/wh1ard/kw-assets.git
cd kw-assets/assets

# Adicione seus arquivos de mídia aqui
cp /caminho/boas-vindas.gif .
cp /caminho/logo.png .
cp /caminho/velociraptor.png .

# Commit e push
git add .
git commit -m "feat: adiciona assets iniciais do bot"
git push origin main
```

Após o push, as URLs já estarão disponíveis instantaneamente.
