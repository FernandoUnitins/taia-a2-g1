# Fase 2: Workflows + contratos

## Propósito de desenvolvimento

Adicionar contrato de dados entre as etapas para garantir formato e qualidade mínima de saída.

## Objetivo

Validar a saída da triagem com `schema_triagem.json` antes de qualquer encaminhamento.

## Entrada, processamento e saída

### Entrada

- Saída intermediária da Fase 1.
- `schema_triagem.json` como contrato formal.

### Processamento

1. Validar cada registro no schema.
2. Identificar registros inválidos.
3. Corrigir erros estruturais quando possível.
4. Revalidar após correções.

### Saída

- Registros válidos para encaminhamento.
- Registro de erros estruturais para auditoria.

## Contrato esperado

Campos obrigatórios:
- `email_id`
- `remetente`
- `titulo`
- `corpo`
- `nomes_relevantes`
- `palavras_chave`
- `prioridade`
- `setor_de_destino`
- `justificativa_classificacao`
- `mensagem_encaminhamento`
- `tool_calls`
- `protocolo_encaminhamento`

## Entrega clara

- Contrato definido em JSON Schema.
- Evidência de validação executada.
- Correção de pelo menos um erro estrutural quando houver.

## Validação simplificada

- Comparar 3 registros de entrada com 3 registros validados.

## Fora do escopo

- Conexão com e-mail real.
- Servidor MCP.

## Critérios de conclusão

- Saída segue o contrato.
- Erros são detectados e documentados.
