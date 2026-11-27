# Configuração eMTA / ONT 192.168.0.1 — Claro / NET

Ferramenta web em arquivo único (`index.html`) com regras específicas de extração para etiquetas Claro / NET:
- **Usuário `192.168.0.1`**: lê logo abaixo da linha `192.168.0.1` / `Usuário:`.
- **Senha do usuário `192.168.0.1`**: fica abaixo do usuário e tem **12 dígitos** (ex.: `B4F2673430B5`).
- **Senha da rede Wi-Fi**: sempre contém **8 dígitos** (ex.: `673430B5`), nunca preenchendo com a senha de 12 dígitos do IP.
- **S/N de 12 dígitos**: prioriza o código de 12 dígitos junto aos códigos de barras de `CM MAC` e `eMTA MAC`.
- **Rodapé estático**: `Criado por: Fernando Sato - Versão 1.5 - 26/11/2026 21:07`.
