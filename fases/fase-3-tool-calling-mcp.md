# Fase 3: Tool calling e MCP Email

## Propósito de desenvolvimento

Demonstrar execução controlada de ações externas no workflow de triagem.

## Objetivo

Executar chamadas de ferramenta para consultar e encaminhar e-mails com rastreabilidade.

## Entrada, processamento e saída

### Entrada

- Registros válidos da Fase 2.
- Definição das ferramentas permitidas.

### Processamento

1. Chamar `consultar_email` para leitura contextual.
2. Chamar `encaminhar_email` para roteamento ao setor.
3. Registrar status de cada chamada em `tool_calls`.
4. Gerar `protocolo_encaminhamento`.

### Saída

- Registros triados com histórico de tool calling.
- Evidências de sucesso, falha ou pendência.

## Ferramentas esperadas

- `consultar_email(email_id)`
- `encaminhar_email(payload)`

## Entrega clara

- Saída final com `tool_calls` por item.
- Protocolo de encaminhamento por e-mail.

## Validação simplificada

- Demonstrar pelo menos 2 chamadas por registro processado.

## Fora do escopo

- Ação irrestrita sem supervisão.
- Ferramentas não autorizadas no workflow.

## Critérios de conclusão

- Tool calls registradas.
- Saída auditável.
- Falhas tratadas sem quebra silenciosa do fluxo.
