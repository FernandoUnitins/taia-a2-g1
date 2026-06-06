# Fase 1: Workflows

## Propósito de desenvolvimento

Transformar a triagem de e-mails em um fluxo de trabalho repetível, com etapas explícitas.

## Entrada, processamento e saída

### Entrada

- Arquivo `emails_entrada.json` com lista de e-mails.
- Cada e-mail deve conter: `email_id`, `remetente`, `titulo`, `corpo`.

### Processamento

1. Ler e-mails de entrada.
2. Extrair campos básicos.
3. Extrair nomes relevantes.
4. Extrair palavras-chave.
5. Inferir prioridade.
6. Inferir setor de destino.
7. Construir mensagem de encaminhamento.

### Saída

- Estrutura intermediária de triagem por e-mail.
- Cada item deve conter classificação e justificativa.

## Passos esperados do workflow

1. Carregar lote de e-mails.
2. Processar item por item.
3. Completar os campos de enriquecimento.
4. Produzir saída intermediária estruturada.

## Entrega clara

- Workflow descrito em markdown.
- Critérios de passagem para a Fase 2 definidos.

## Validação simplificada

- Verificar se todos os e-mails geraram estrutura base com classificação.

## Fora do escopo

- Validação formal por schema.
- Encaminhamento por ferramenta externa.

## Critérios de conclusão

- Etapas estão explícitas.
- Há rastreabilidade mínima por e-mail.
