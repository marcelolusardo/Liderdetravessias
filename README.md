# Lider de Travessias (site)

Site institucional de Marcelo Lusardo, publicado em **liderdetravessias.com.br**.

Páginas: home (`index.html`), Quem é Marcelo (`marcelo-lusardo.html`), Expert Education (`expert-education.html`) e Notícias (`noticias.html`). Site estático, sem build.

## Notícias
`scripts/build-noticias.mjs` gera `assets/data/noticias.json` a partir de feeds reais. O workflow `.github/workflows/update-noticias.yml` roda só manualmente ("Run workflow"): o agendamento está desligado para não sobrescrever os vídeos escolhidos à mão.

## Antes de liberar para o Google
As páginas estão com `noindex` e o `robots.txt` bloqueia tudo (`Disallow: /`). Para indexar: trocar por `Allow: /`, adicionar a linha `Sitemap:` e remover `<meta name="robots" content="noindex, nofollow">`.
