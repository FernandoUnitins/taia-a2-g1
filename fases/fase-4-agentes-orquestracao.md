# Fase 4: Agentes e orquestração controlada

## Propósito de desenvolvimento

Descrever a evolução para um agente orquestrador mantendo limites de autonomia.

## Objetivo

Permitir que um agente execute o workflow completo da triagem sem violar contratos ou regras de negócio.

## Controles esperados

- Limite de iterações por lote.
- Ferramentas permitidas explicitamente.
- Contrato obrigatório antes de encaminhar.
- Registro de incertezas e bloqueios.

## Passos esperados do workflow

1. Ler missão operacional da triagem.
2. Carregar entradas permitidas.
3. Executar fases 1, 2 e 3 na ordem.
4. Interromper quando houver falha crítica.
5. Gerar relatório final de execução.

## Entrega clara

- `log_execucao_triagem.md`
- `relatorio_validacao_triagem.md`

## Validação simplificada

- Demonstrar que o agente respeita contratos e limites de ferramenta.

## Fora do escopo

- Autonomia irrestrita.
- Execução de ações não auditáveis.

## Critérios de conclusão

- Orquestração reproduzível.
- Limites e responsabilidades explícitos.
