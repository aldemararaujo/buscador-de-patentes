# Buscador de Patentes

Aplicativo de página única (HTML/JS puro, sem build, sem dependências externas) para buscar patentes reais por palavra-chave.

## Como usar

1. Abra `buscador-de-patentes.html` diretamente no navegador (duplo clique).
2. Crie uma conta gratuita em [developers.epo.org](https://developers.epo.org) e registre um app para gerar seu **Consumer Key** e **Consumer Secret** do EPO Open Patent Service (OPS).
3. Clique no ícone de engrenagem (⚙) no app e cole as duas chaves. Elas ficam salvas só no `localStorage` do seu navegador — nunca saem da sua máquina.
4. Busque por palavras-chave. Os resultados vêm em tempo real da base bibliográfica da EPO (cobertura de mais de 90 escritórios de patentes, incluindo INPI/Brasil, USPTO, WIPO/PCT).

## O que o app faz

- Busca por texto livre (título + resumo + reivindicações), com filtro opcional para Brasil/INPI.
- Lista de resultados com título, número, data, titular, classificação IPC/CPC e link real para o Espacenet.
- Paginação real.
- Tela de detalhe com resumo e família de patentes buscados ao vivo.
- Lista de salvos (localStorage), com exportar/importar em `.json`.

Nenhum dado é inventado: campos ausentes na resposta da API aparecem como "não informado".

## Licença

Uso pessoal.
