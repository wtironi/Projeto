name: Deploy HTML no GitHub Pages

on:
  push:
    branches:
      - main  # Executa o workflow quando houver um push na branch main

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout do código
        uses: actions/checkout@v3  # Obtém o código do repositório

      - name: Criar diretório de build
        run: mkdir public && cp index.html public/  # Move o index.html para um diretório público

      - name: Deploy no GitHub Pages
        uses: JamesIves/github-pages-deploy-action@v4
        with:
          branch: gh-pages  # Faz o deploy na branch gh-pages
          folder: public  # Pasta que será enviada para o GitHub Pages
