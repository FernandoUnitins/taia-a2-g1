# Implementacao do Projeto - Triagem de E-mails de Suporte

## Escopo aplicado
Esta implementacao segue o formato solicitado em aula:
1. Contexto operacional (POP de triagem de e-mails)
2. Workflow em markdown
3. Workflow com contratos
4. Tool calling com rastreabilidade
5. Orquestracao controlada

## Artefatos principais
- workflow_triagem.md
- .agents/workflows/triagem-email-suporte.yaml
- fases/fase-0-skills.md
- fases/fase-1-workflows.md
- fases/fase-2-workflows-contratos.md
- fases/fase-3-tool-calling-mcp.md
- fases/fase-4-agentes-orquestracao.md
- schema_triagem.json
- emails_entrada.json

## Estrutura por fases implementadas

### Fase 0 - Base
- Define problema, escopo, limites e artefatos da trilha.

### Fase 1 - Workflow
- Entrada: emails_entrada.json
- Processamento: leitura, extração, classificação e construção da mensagem
- Saída: estrutura intermediária com triagem por e-mail

### Fase 2 - Workflow + contratos
- Entrada: saída intermediária + schema_triagem.json
- Processamento: validação contratual, detecção e correção de inconsistências
- Saída: registros válidos para encaminhamento

### Fase 3 - Tool calling
- Entrada: registros validados
- Processamento: consultar_email, encaminhar_email, registro de tool_calls
- Saída: protocolo de encaminhamento e trilha de auditoria

### Fase 4 - Orquestração
- Entrada: missão operacional da triagem
- Processamento: execução ordenada das fases com regras de parada
- Saída: logs e relatório de validação

## Entrada e saída conforme modelo da aula

### Entrada formal
- emails_entrada.json
- schema_triagem.json

### Saída formal
- saida_triagem.json
- log_execucao_triagem.md
- relatorio_validacao_triagem.md

## Observação para Antigravity
O ponto de entrada da execução é o arquivo workflow_triagem.md, que referencia o arquivo YAML com etapas, contratos, restrições e validações.
