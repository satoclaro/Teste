# Configuração eMTA / ONT 192.168.0.1 — Claro / NET

Ferramenta web em arquivo único (`index.html`) otimizada para extração rápida e precisa por captura de foto:
- **Recorte ampliado nas credenciais**: além da etiqueta inteira, faz leitura ampliada (`2.1x`) na área inferior onde ficam `IP: 192.168.0.1`, `Usuário: CLARO_...`, `Senha: ...` e `SSID 2.4GHz / 5GHz / SENHA`.
- **Diferenciação entre senha de acesso (`192.168.0.1`) e senha Wi-Fi**: associa corretamente cada `Senha:` ao seu respectivo bloco (usuário/IP vs. SSID/Wi-Fi).
- **S/N separado de código de barras e MACs**: filtra MACs (`CM MAC` / `eMTA MAC`) e códigos de barras colados.
- **Rodapé estático**: `Criado por: Fernando Sato - Versão 1.4 - 26/11/2026 20:53`.
