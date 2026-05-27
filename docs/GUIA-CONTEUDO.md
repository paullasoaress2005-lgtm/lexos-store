# Guia rapido da LEX.OS Store

Este marketplace foi montado para ser editavel sem mexer no HTML.

## Onde alterar produtos, precos e links

Edite o arquivo:

`data/catalogo.json`

Cada item em `products` vira um card na pagina `/plugins`. Para cadastrar um novo produto, duplique um bloco e altere:

- `id`: identificador interno, sem espacos.
- `number`: numero exibido no card.
- `status`: por exemplo `Disponivel`, `Lista de interesse` ou `Em construcao`.
- `category`: use `Plugin`, `Pacote`, `Treinamento` ou `Agente`.
- `name`: nome curto do produto.
- `title`: titulo comercial.
- `summary`: explicacao curta.
- `price`: preco exibido.
- `terms`: condicao exibida abaixo do preco.
- `checkoutUrl`: link de pagamento da Kirvano.
- `commands`: comandos ou capacidades do pacote.
- `features`: lista de beneficios e componentes.

## Como colocar o link do grupo do WhatsApp

O link fica em um unico campo:

`whatsappGroupUrl`

Todos os botoes com `data-whatsapp-group` usam esse endereco automaticamente. O link atual ja esta configurado:

`https://chat.whatsapp.com/Cc0oM8GN2aJGudB9Q4MQZm?mode=gi_t`

## Como ligar cada pacote ao checkout da Kirvano

1. Crie sua conta em `https://app.kirvano.com/signup`.
2. Cadastre o produto na Kirvano.
3. Abra o produto e copie o link de checkout da oferta.
4. Cole esse link no campo `checkoutUrl` do produto correspondente.

Enquanto `checkoutUrl` estiver vazio, o botao do produto leva para o WhatsApp de atendimento da LEX.OS.

## Como publicar conteudos

A pagina `/conteudos` le a lista `contents` em `data/catalogo.json`.

Para adicionar conteudo, duplique um item e altere:

- `tag`: tipo do material, como Guia, Checklist ou Fluxo.
- `title`: titulo.
- `description`: resumo.
- `url`: link para abrir o material.

Em uma proxima etapa, esses conteudos podem virar arquivos HTML proprios, posts em CMS ou links para Notion/Drive.

## Rotas internas

- `/` abre a loja.
- `/plugins` abre o catalogo completo.
- `/conteudos` abre a biblioteca.
- `/comunidade` abre a pagina do grupo.
