# triso-docs
Repositorio criado para manter documentações.

## Deploy (DigitalOcean App Platform - Static Site)

O conteúdo publicado é a pasta `public/`. A spec está em [.do/app.yaml](.do/app.yaml). O [package.json](package.json) mínimo (sem scripts de build) existe apenas para o App Platform detectar o projeto.

Pelo painel: Create > Apps > GitHub > `trisot3c/triso-docs` (branch `main`) > tipo **Static Site** > Source Directory `/` > Output Directory `public` > sem Build Command.

Pelo CLI:

```
doctl apps create --spec .do/app.yaml
```

A política fica em `https://<app>.ondigitalocean.app/policy/`. Cada push na `main` faz novo deploy.
