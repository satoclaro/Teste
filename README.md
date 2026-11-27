# Configuração eMTA / ONT 192.168.0.1 — Claro / NET

Ferramenta web em arquivo único (`index.html`) otimizada para extração rápida em passada única:
- **Modo turbo (1 passada OCR)**: pré-aquece o worker ao carregar a página e reduz a resolução máxima para `1440px–1500px`, tornando a leitura da foto bem mais rápida.
- **Senha do usuário `192.168.0.1`**: busca logo abaixo da linha do usuário e prioriza valores de `8` a `13` caracteres (como o padrão de `12` dígitos `B4F2673430B5`).
- **S/N de 12 dígitos junto aos códigos de barras**: prioriza o código alfanumérico de `12` caracteres próximo a `S/N` e aos códigos de barras de `CM MAC` / `eMTA MAC`, sem confundir com MACs.
- **Rodapé estático**: `Criado por: Fernando Sato - Versão 1.5 - 26/11/2026 21:07`.
