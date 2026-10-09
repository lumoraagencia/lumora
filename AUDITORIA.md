# Auditoria do gerador e dos apps — 9 de outubro de 2026

## Correções

- Geração por sentença, com até três alvos diferentes por sentença. O modo Completa é padrão; Essencial e Equilibrada permitem diminuir o volume. A revisão mostra estimativas por módulo antes de gerar.
- Questões de lacuna, verdadeiro/falso e vários grupos de associação. Casos de aplicação continuam restritos a regras condicionais expressas no material.
- Termos e trechos repetidos não multiplicam exercícios. A validação rejeita alternativas duplicadas, respostas sem fonte, índices incorretos e associações sem referência válida.
- As referências mantêm o trecho literal. No texto integral, a sentença da questão recebe realce dentro do parágrafo original.
- Sessões de estudo terminam em uma tela de resultados. O cronômetro encerra simulados mesmo fora da aba de questões e recusa respostas enviadas depois do prazo.
- Respostas em digitação e associações são preservadas durante atualizações da interface. Trocar módulo ou filtros finaliza o simulado em andamento.
- Embaralhamento com Fisher–Yates. Uma animação de swipe atrasada não pode avaliar a carta seguinte após um clique no botão. Histórico de desfazer limitado às últimas 20 cartas para conter consumo de memória.
- Salvamento captura a identificação do material junto com os dados, evitando gravar progresso na chave de outro material.
- Cada app exportado possui banco de dados próprio. O cache offline só limpa versões antigas do seu próprio endereço, preservando outros apps.
- HTML portátil inicia mesmo sem acesso ao armazenamento local; tema não bloqueia a inicialização. Exportação preserva caracteres especiais da fonte, permite reexportar sem duplicar o script de conteúdo e personaliza o nome no manifest.

## Verificações

Suíte final: 36 testes aprovados. Lacunas idênticas com respostas diferentes na fonte são descartadas para evitar questões ambíguas, sem interromper a geração dos demais itens.

- Suíte de testes cobre extração EPUB e Office textual, segmentação, geração, validade das referências, duplicatas, XP, flashcards, desfazer, respostas, simulados, sete abas, fontes e exportação.
- O HTML portátil é executado em um ambiente DOM: inicia e navega pelas sete abas mesmo em contexto file:// sem IndexedDB.
- Teste de volume: 12 parágrafos, 36 sentenças, 108 flashcards e 123 questões em um módulo; Essencial estima 36 flashcards para o mesmo material. São dados sintéticos de teste, não uma promessa de quantidade mínima para qualquer documento.
- Navegador: upload, revisão, alteração de densidade, geração e questão errada com retorno ao material verificados em largura de 390 px. Isso não substitui testes em aparelhos físicos.

## Limites que permanecem

A geração é local e extrativa: usa recuperação literal e regras explícitas, sem compreensão por IA externa. A quantidade depende da extensão, legibilidade e variedade do material. Aumentar o número de exercícios não garante a qualidade pedagógica de cada escolha de palavra. OCR pode conter erros e precisa de conferência.

DOC/PPT e fidelidade visual Office precisam do conversor local. GitHub Pages não executa esse conversor. O teste nativo do Office/LibreOffice e a instalação em aparelhos físicos iPhone/Android continuam pendentes. Nenhum conjunto finito de testes garante funcionamento perfeito com todos os arquivos ou navegadores. Os testes documentam os cenários efetivamente cobertos.

Para usar a nova quantidade de exercícios em um app criado antes desta versão, envie o material ao gerador novamente e baixe um novo pacote. Pacotes já baixados não se modificam sozinhos; uma nova geração pode ter identidade e progresso diferentes.
