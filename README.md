# Buscador de Patentes

Aplicativo web de busca de patentes conectado à API oficial do **EPO — Open Patent Services (OPS)**, a base do Espacenet. Feito para pesquisadores que precisam fazer uma primeira busca de anterioridade ou explorar o estado da técnica sem depender de software instalado.

**➡️ Use online: <https://aldemararaujo.github.io/buscador-de-patentes/>**

## O que ele faz

- **Busca em linguagem natural**, em português ou inglês. O termo digitado é traduzido automaticamente para o inglês e a busca cobre os dois idiomas — assim o acervo internacional (majoritariamente em inglês) não fica de fora.
- **Filtro "somente patentes BR"** para restringir a documentos depositados no Brasil.
- **Detalhe de cada documento** em abas: dados bibliográficos (título, requerentes, inventores, classificação IPC/CPC, resumo) e **família da patente** (depósitos correspondentes em outros países).
- **Lista de salvos**: marque documentos de interesse e exporte/importe a lista em JSON para continuar em outro computador.
- **Link direto para o Espacenet** em cada resultado, para aprofundar a análise.

## Como começar (chave gratuita da EPO)

O app **não vem com nenhuma chave embutida** — cada pessoa usa a sua, gratuita:

1. Crie uma conta em <https://developers.epo.org>.
2. Crie um "app" no painel — ele gera um **Consumer Key** e um **Consumer Secret**.
3. No Buscador, clique no botão ⚙ **Configurar** e cole a chave e o segredo.

Pronto: a cota gratuita da EPO é suficiente para uso individual de pesquisa.

## Privacidade

- Sua chave fica salva **apenas no seu navegador** (localStorage). Ela não é enviada para nenhum servidor além da própria EPO, no momento da autenticação.
- Não há backend próprio, cadastro, cookies de rastreamento nem coleta de dados: o navegador conversa diretamente com a API da EPO.

## Rodando localmente

É um arquivo único e sem dependências: baixe o `index.html` e abra no navegador. Funciona offline, exceto (claro) as chamadas à API da EPO e a tradução automática.

## Limitações conhecidas

- A busca usa o campo `txt` (título, resumo e reivindicações) do OPS; uma busca de anterioridade completa deve combinar outras bases (INPI, WIPO Patentscope, Lens.org) e estratégias por classificação IPC/CPC.
- A cota gratuita do OPS tem limite de volume; HTTP 403 normalmente indica cota excedida ou chave inválida.

## Licença

[MIT](LICENSE) — use, adapte e compartilhe à vontade, mantendo o aviso de copyright.
