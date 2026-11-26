# Configuração eMTA / ONT 192.168.0.1 — Claro / NET

Ferramenta web em arquivo único (`index.html`) otimizada para extração rápida e precisa por captura de foto:
- **Execução mais rápida**: pipeline enxuto em 3 etapas (`BarcodeDetector` + OCR contraste `1.65x` + OCR binarizado `1.75x`) com captura imediata.
- **Senhas logo abaixo**: captura a senha do IP `192.168.0.1` na linha imediatamente abaixo do usuário e a senha do Wi-Fi na linha logo abaixo do SSID / usuário Wi-Fi (`2.4 GHz` / `CLARO_` / `NET_`), com ou sem rótulo explícito.
- **S/N separado de código de barras e MACs**: filtra MACs (`CM MAC` / `eMTA MAC`) e códigos de barras numéricos colados na mesma linha do `S/N`.
- **4 campos de cópia rápida no topo**, arquivamento local e exportação/importação em CSV, JSON e PDF.
- **Rodapé estático**: `Criado por: Fernando Sato - Versão 1.3 - 26/11/2026 20:38`.
