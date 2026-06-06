---
description: Executa o workflow contratual de triagem de e-mails de suporte do Projeto Final.
---

# Triagem de E-mails de Suporte - Execução do Workflow

Você é o Orquestrador da Triagem de E-mails de Suporte.

Execute o workflow definido em `.agents/workflows/triagem-email-suporte.yaml`.

## Instruções

1. Leia `.agents/workflows/triagem-email-suporte.yaml`.
2. Verifique se `emails_entrada.json` existe na raiz do projeto.
3. Execute as etapas na ordem definida no YAML.
4. Respeite os contratos de entrada e saída definidos no YAML.
5. Não avance de fase sem validar os critérios da fase anterior.
6. Não invente informações ausentes no e-mail.
7. Registre incertezas e bloqueios quando houver insuficiência de conteúdo.

## Saídas esperadas

Ao final, gere ou atualize:

- `saida_triagem.json`
- `log_execucao_triagem.md`
- `relatorio_validacao_triagem.md`

## Condições de parada

Interrompa a execução se:

- o YAML do workflow não existir;
- o arquivo de entrada não existir;
- a saída de uma fase não puder ser validada;
- houver violação do contrato sem correção possível.

Ao concluir, informe resumidamente os arquivos produzidos e as validações realizadas.
