# Configuração eMTA / ONT 192.168.0.1 — Claro / NET

Ferramenta web em arquivo único (`index.html`) otimizada para leitura rápida e precisa de etiquetas Claro / NET:
- **Anti-confusão entre `6`, `8` e `B` na senha Wi-Fi (8 caracteres):** ajusta o contraste sem estourar os traços e confere o sufixo hexadecimal do SSID (`CLARO_2G...` / `CLARO_5G...`) para evitar que `6` ou `B` virem `8` (ex.: `673430B5` em vez de `87343085`).
- **Usuário e senha do `192.168.0.1`:** lê o usuário logo abaixo de `192.168.0.1` e a senha de 12 dígitos abaixo do usuário.
- **S/N de 12 dígitos:** prioriza o código de 12 dígitos junto aos códigos de barras de `CM MAC` e `eMTA MAC`.
- **Rodapé estático:** `Criado por: Fernando Sato - Versão 1.5 - 26/11/2026 21:07`.
