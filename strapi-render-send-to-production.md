# Deploy Strapi on Render.com

## Passo 1
Criar banco de dados em produção

## Passo 2
No render.com, criar novo Web Service

## Passo 3
Conectar ao repositório no github

## Passo 4
Adicionar informações do web service, da seguinte forma:

Name: Coloque o nome do web-service
Region: Não alterar
Branch: Não alterar
Root Directory: Não alterar
Environment: Não alterar
Build Command: yarn && NODE_ENV=production yarn build
Start Command: Não alterar

## Passo 5
Antes de criar o web service, aperte em advanced e selecione secret file para adicionar o conteúdo de .env

## Passo 6
Ir em custom domains, e adicionar api.DOMINIO_CUSTOMIZADO.com

## Passo 7
Ir no provedor do dominio e adicionar uma chave CNAME com api e o valor pegar direto do local onde adicionar custom domain

## Passo 8
Lembrar de colocar no .env informações nos campos:
PUBLIC_SERVER_URL=
PUBLIC_ADMIN_URL=

## Passo 9
Criar um novo static site

## Passo 10
Selecionar o mesmo repositório escolhido anteriormente

## Passo 11
Adicionar informações do static site, da seguinte forma:

Name: Coloque o nome do static-site
Branch: Não alterar
Root Directory: Não alterar
Build Command: yarn && NODE_ENV=production yarn build
Publish directory: ./dist/build

## Passo 12
Antes de criar o static site, aperte em advanced e selecione secret file para adicionar o conteúdo de .env


## Passo 13
Ir na opção redirects/rewrite, selecionar rewrite e no primeiro campo colocar /* e no segundo /index.html