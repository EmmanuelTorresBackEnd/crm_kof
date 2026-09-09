# CRM em Kof

Sistema de CRM iniciado em Kof. O projeto foi organizado para crescer por modulos, mantendo a API, o dominio e a persistencia separados.

## Modulos

- usuarios: autenticacao, papeis e permissoes
- organizacoes: empresas e equipes
- contatos: pessoas relacionadas a empresas
- leads: entrada e qualificacao de oportunidades
- pipeline: negocios, etapas, valores e previsao
- atividades: tarefas, ligacoes, reunioes e notas
- comunicacoes: historico de interacoes
- relatorios: indicadores comerciais

## Estrutura

```text
crm/
  README.md
  docs/
    DOMAIN.md
  db/
    schema.sql
  src/
    main.kf
```

## Rodar

A partir da pasta que contem a distribuicao do Kof:

```powershell
.\kof-0.2.8-beta-windows-x86_64\bin\kof.bat serve .\crm\src\main.kf --port 8080
```

Depois, abra `http://localhost:8080/health`.

## Estado atual

Esta primeira entrega cria o contrato inicial da API e o modelo de dados. Os endpoints ainda retornam respostas de referencia; o proximo passo e conectar o repositorio ao SQLite e adicionar autenticacao.
