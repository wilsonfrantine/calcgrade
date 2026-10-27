# Simulador de notas

Simulador estático de médias para estudantes. A aplicação e seus arquivos de configuração ficam em [`docs/`](docs/), publicada diretamente pelo GitHub Pages.

## Usar

- A página inicial abre um simulador livre com três avaliações. É possível escolher média aritmética ou ponderada e adicionar ou remover avaliações.
- Para abrir uma configuração específica, use `?id=<nome>`. Por exemplo: `?id=2026_fisio_humana` carrega `docs/configs/2026_fisio_humana.json`. O sufixo `.json` também é aceito.
- Se a configuração não existir ou não puder ser carregada, a página informa o problema e permite voltar ao simulador livre.

## Configurações

Adicione os arquivos JSON em `docs/configs/`. O identificador usado na URL corresponde ao nome do arquivo, sem a extensão. Consulte [`2026_fisio_humana.json`](docs/configs/2026_fisio_humana.json) como exemplo de estrutura e configuração.

## Pré-visualização local

Sirva a pasta `docs/` com um servidor HTTP local para que o carregamento dos JSONs funcione. Com Node.js e `npx` instalados:

```sh
npx live-server docs --port=8080
```

Depois, abra `http://127.0.0.1:8080/` no navegador.

## Publicação

Nas configurações do repositório, escolha **Settings → Pages → Build and deployment → Source: Deploy from a branch**, selecione `main` e a pasta `/docs`. Os pushes para `main` serão publicados automaticamente.
