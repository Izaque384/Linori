# Linori — Estúdio de catálogos PDF

A Linori transforma fotos, nomes e descrições de produtos em **catálogos PDF A4 de alta qualidade**, que o comerciante poderá baixar e compartilhar onde quiser.

## Proposta comercial

- Criar o catálogo e visualizar uma prévia gratuitamente.
- **Pagamento único por catálogo** para liberar o download do PDF final.
- Sem assinatura, sem mensalidade, sem catálogo hospedado e sem loja virtual.
- O preço de **R$ 49,90** exibido no MVP é uma hipótese e **não representa cobrança ativa**.

## MVP v0.2 — funciona agora

- Site responsivo, editor de marca, upload local de fotos JPG/PNG/WebP.
- Até 16 produtos com nome, descrição, categoria e preço opcional.
- Reorganização e edição dos produtos.
- Três estilos: Lilás Noturno, Editorial Areia e Grafite Minimal.
- Prévia paginada: capa, dois produtos por página e contato.
- Exportação de PDF A4 demonstrativo **com marca d'água**.
- Rascunhos salvos no IndexedDB do navegador, quando disponível.
- Arquivo único `index.html` sem dependências externas: pode ser hospedado na Cloudflare Pages.

## Ainda não disponível

**Checkout, verificação de pagamento, upload persistente no servidor e download comercial desbloqueado não estão implementados.**

A versão de produção deverá:

1. Receber e armazenar as imagens de forma segura.
2. Processar o pagamento com um provedor (ex.: Stripe), via backend.
3. Verificar a confirmação por webhook autenticado.
4. Gerar o PDF final no servidor, sem marca d'água.
5. Entregar URL de download temporária e protegida, vinculada ao pagamento aprovado.
6. Definir prazos para baixar, política de retenção, limites de uso e suporte.

**Não liberar o PDF final apenas com estado do navegador, link manipulável ou botão habilitado por JavaScript.** Na produção também será importante oferecer texto selecionável, imagens de maior resolução e tratamento de fotos baixas em qualidade.

## Testar

Abra `index.html` no navegador ou publique diretamente como site estático.

A versão atual é uma demonstração funcional do editor de PDFs, não uma operação comercial pronta.
