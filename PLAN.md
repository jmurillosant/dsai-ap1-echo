# Plano de Arquitetura - Echo

## Stack
- Backend: Python 3 + Django
- Banco: PostgreSQL (Neon em producao, Postgres local em dev)
- Frontend: Django Templates + HTML + CSS puro
- Hospedagem: Render.com (app) + Neon (banco)
- Servidor: Gunicorn + Whitenoise

## Ordem de Implementacao
1. Setup Django + app core
2. Conta e autenticacao (cadastro, login, logout)
3. Posts (texto + imagens)
4. Linha do tempo e perfis publicos
5. Interacoes (curtir, responder, repostar)
6. Relacoes sociais (seguir, deixar de seguir)
7. Testes expansivos e seed de dados

## Restricoes
- Codigo deve passar de 100 mil linhas no cloc
- Sem React, sem API REST separada
- Tudo server-side rendered
