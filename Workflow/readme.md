# Fluxo de trabalho do n8n - Envio de email

## Descrição
Este fluxo de trabalho envia um email quando o gatilho "Test workflow" é acionado.

## Nodes

### 1. Rodando a aplicação

- Instalando o n8n localmente:

  `npm install n8n -g`

- Rodando localmente:

  `npx n8n`

### 2. Manual Trigger: When clicking "Test workflow"
- Tipo: `n8n-nodes-base.manualTrigger`
- Ao clicar neste gatilho, o fluxo de trabalho é acionado.

### 3. Send Email
- Tipo: `n8n-nodes-base.emailSend`
- Este nó envia um email.
- Parâmetros:
  - De: `pedrogabriel12423@gmail.com`
  - Para: `pedrogabriel.pix@hotmail.com`
  - Assunto: `Apenas um teste`
  - Corpo HTML: `<h1>Um mero teste</h1>`
  
## Exemplo de Dados de Entrada
```json
{
  "Send Email": [
    {
      "json": {
        "name": "First item",
        "code": 1
      }
    },
    {
      "json": {
        "name": "Second item",
        "code": 2
      }
    }
  ]
}
