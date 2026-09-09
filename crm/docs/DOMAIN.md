# Dominio do CRM

## Usuario

Representa quem acessa o sistema. Possui nome, email, senha protegida, status, papel e equipe.

## Organizacao

Empresa ou conta atendida pelo CRM. Pode ter varios contatos, leads e negocios.

## Contato

Pessoa ligada a uma organizacao. Guarda nome, email, telefone, cargo e preferencias de contato.

## Lead

Potencial cliente que ainda nao foi convertido. Tem origem, status, responsavel, pontuacao e proxima atividade.

Estados sugeridos: `novo`, `contactado`, `qualificado`, `desqualificado`, `convertido`.

## Negocio

Oportunidade comercial associada a uma organizacao e, opcionalmente, a um contato. Tem pipeline, etapa, valor, probabilidade e previsao de fechamento.

## Atividade

Acao planejada ou concluida: tarefa, ligacao, reuniao, email ou nota. Pode ser relacionada a um lead, contato ou negocio.

## Auditoria

Registra alteracoes importantes para rastreabilidade: usuario, entidade, acao, dados anteriores e novos dados.

## Fluxo principal

```text
Lead novo -> qualificacao -> conversao -> negocio -> ganho/perda
                         \-> contato + organizacao
```

## API inicial

- `GET /health`
- `GET /api/users`
- `GET /api/leads`
- `POST /api/leads`
- `GET /api/contacts`
- `GET /api/organizations`
- `GET /api/deals`
- `GET /api/activities`
