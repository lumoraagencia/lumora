# Lumora

Gerador de aplicativos de estudo com conteúdo rastreável ao material original.

**[Abrir o gerador](https://lumoraagencia.github.io/lumora/)**

1. Abra o gerador e escolha seu arquivo.
2. Revise os módulos detectados.
3. Gere o app de estudo, use a prévia e baixe o pacote offline.

## Código completo

Baixe [Lumora-Codigo-Completo.zip](./Lumora-Codigo-Completo.zip) e extraia o conteúdo. O pacote inclui código modular, dependências de leitura/OCR, aplicação compilada, testes e documentação. Consulte `README.md`, `ENTREGA.md` e `VALIDACAO.md` dentro dele.

Com Node.js 24 instalado:

```sh
npm ci
node build.mjs
node server.mjs
```

Abra http://127.0.0.1:4173. No Windows, também é possível usar `Iniciar-Lumora.cmd`.

## Recursos e limites

- Sete abas: flashcards, questões, tabelas, resumos, mapa mental, material original e progresso.
- PDF, imagens com OCR, TXT, Markdown e EPUB são processados no navegador; DOCX/PPTX/RTF possuem leitura de conteúdo textual.
- Conversão visual nativa de Office/DOC/PPT requer o servidor local e Office ou LibreOffice; não está disponível no GitHub Pages.
- O progresso e os materiais enviados ficam no dispositivo. A geração usa trechos do arquivo, sem envio a uma IA externa.
- O ZIP gerado inclui uma versão HTML portátil. A instalação como PWA exige acesso por HTTPS ou localhost; não funciona por `file://`.
- A validação em aparelhos físicos iPhone/Android e a conversão Office nativa permanecem pendentes. Consulte o relatório completo no pacote.

## Publicação

O fluxo `.github/workflows/pages.yml` extrai o pacote, instala as dependências de teste, compila, executa os testes e publica `dist` no GitHub Pages. Para uma atualização completa, substitua o ZIP mantendo sua estrutura interna.
