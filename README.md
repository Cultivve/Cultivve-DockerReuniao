# Cultivve - Selenium Grid Docker

Ambiente de automação de testes web distribuído usando Selenium Grid com Docker.

## Para que serve

Configura um Selenium Hub com um nó Chrome para rodar testes de automação web em paralelo.

- **Selenium Hub**: Gerencia e distribui os testes (porta 4444)
- **Chrome Node**: Executa os testes no navegador Chrome (porta 7900 para debug visual)

## Como subir

```bash
docker compose up -d
```

Para verificar se está rodando:

```bash
docker compose ps
```

Para parar:

```bash
docker compose down
```

## Acessos

- **Selenium Grid Console**: http://localhost:4444
- **VNC Debug Chrome**: http://localhost:7900 (senha: `secret`)

## Configurações

O arquivo `docker-compose.yml` define:

- Máximo de 4 sessões simultâneas
- Timeout de 60 segundos
- Nó Chrome com 2 sessões simultâneas
- Memória compartilhada de 2GB para o Chrome
- Volume para perfil Chrome em `./chrome-profile`
