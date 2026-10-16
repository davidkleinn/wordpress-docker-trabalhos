# WordPress com Docker: duas topologias

Implementações realizadas para as atividades de configuração de WordPress com Docker.

## Projetos

| Diretório | Proposta | Acesso |
| --- | --- | --- |
| `Trabalho-1-WordPress-Docker` | WordPress e MySQL 5.7 em contêineres Docker individuais | `http://localhost:8080` |
| `Trabalho-2-WordPress-Nginx-Compose` | Nginx com balanceamento para três instâncias WordPress e um MySQL compartilhado, via Docker Compose | `http://localhost` |

## Validação realizada

As duas topologias foram iniciadas localmente no Docker Desktop. O primeiro trabalho apresentou o painel do WordPress na porta `8080`. O segundo iniciou os cinco serviços esperados (`nginx`, `wordpress1`, `wordpress2`, `wordpress3` e `mysql`) e apresentou o painel por meio do Nginx na porta `80`.

## Como executar

Consulte o `README.md` de cada diretório. Em resumo:

```powershell
# Trabalho 1
cd .\Trabalho-1-WordPress-Docker
powershell -ExecutionPolicy Bypass -File .\executar-trabalho-1.ps1

# Trabalho 2
cd ..\Trabalho-2-WordPress-Nginx-Compose
Copy-Item .env.example .env
powershell -ExecutionPolicy Bypass -File .\validar.ps1
```

## Tecnologias

- Docker Desktop e Docker Compose
- WordPress
- MySQL 5.7
- Nginx 1.19.0
- PowerShell

> As credenciais presentes em `.env.example` são exclusivamente as credenciais didáticas previstas no enunciado. Para qualquer ambiente real, utilize segredos próprios e não versione o arquivo `.env`.
