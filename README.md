# Linori — catálogo digital com contato direto pelo WhatsApp

**Status: MVP de demonstração, ainda sem pagamentos nem publicação real de catálogos.**

## Proposta definida

- O lojista monta o catálogo gratuitamente.
- Um pagamento **único** libera a publicação após confirmação segura no backend.
- Cada produto possui seu próprio botão **Consultar no WhatsApp**, com mensagem pré-preenchida, identificando o produto.
- **Não há carrinho, checkout dos produtos ou cobrança de mensalidade.**
- Não prometer hospedagem irrestrita ou vitalícia. Definir política de uso, limites e continuidade antes da venda.

## O que funciona neste protótipo

- Landing responsiva com identidade lilás da Linori.
- Editor de loja com nome, descrição, WhatsApp e Instagram.
- Cadastro/edição/exclusão de produtos, foto otimizada localmente, categoria, preço e disponibilidade.
- Três temas visuais e prévia em tempo real, inclusive em tela cheia.
- Cada botão de WhatsApp gera `https://wa.me/55DDDNUMERO?text=...` com a consulta relativa àquele produto. É necessário cadastrar um número válido.
- Rascunho salvo no `localStorage` do navegador, com importação/exportação em JSON.

## O que ainda NÃO funciona

- Conta/autenticação e banco de dados multiusuário.
- Pagamento real ou concessão de acesso por pagamento.
- Hospedagem de imagens ou catálogos no servidor.
- Publicação por slug/link público e gestão de links.

A tela “Liberar publicação” **não cobra**: explica explicitamente as dependências pendentes. Não conecte um botão de pagamento estático sem validar o pagamento no servidor por webhook.

## Rodar localmente

Abra `index.html` em navegador moderno, ou rode um servidor local:

```bash
python -m http.server 8080
```

Visite `http://localhost:8080`.

## Hospedagem da DEMO no Cloudflare Pages

- Framework: **None**
- Branch: `main`
- Comando de build: `exit 0`
- Diretório de publicação: `/`

O deploy estático deixa apenas a demonstração online. Para o SaaS real, adicionar autenticação, armazenamento, validação de catálogo e checkout com confirmação por webhook antes de liberar publicação.

## Próxima etapa (MVP comercial)

1. Autenticação individual de lojistas e autorização por proprietário.
2. Tabelas `accounts`, `catalogs`, `products`, `purchases`, `payment_events`.
3. Upload seguro/compressão de imagens e limites de uso.
4. Pagamento único com checkout hospedado e **webhook validado**; publicação transacional e idempotente.
5. Rota pública `/c/:slug`, apenas para catálogos com pagamento confirmado.
6. Tratamento LGPD, termos comerciais, política de hospedagem e remoção/portabilidade.

Preço de R$ 49,90 é apenas uma hipótese para validação, não cobrança ativa.