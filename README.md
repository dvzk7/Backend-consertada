# Backend StumbleBeast — versão corrigida

## Correção

A raiz (`GET /`) agora retorna um JSON de status, e `GET /api/v1/ping` foi movido para antes do middleware global de autenticação. As rotas de jogo continuam protegidas pelo middleware `authenticate`. A rota pública existente `GET /version/get` continua disponível.

## Deploy no Render

1. Envie o conteúdo deste projeto para o repositório conectado ao serviço no Render (ou substitua os arquivos correspondentes).
2. Confirme que o **Root Directory** do serviço aponta para a pasta que contém `package.json`.
3. Use `npm install` como Build Command e `npm start` como Start Command.
4. Cadastre no painel do Render as variáveis de ambiente necessárias usando os valores já guardados com segurança; não publique o arquivo `.env`.
5. Faça um novo deploy e verifique `GET /` (status JSON), `GET /api/v1/ping` (`OK`) e `GET /version/get` (versão criptografada).

O Render fornece `PORT` automaticamente; o servidor usa `process.env.PORT` quando disponível.
