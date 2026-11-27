# Claro OCR Campo - 192.168.0.1 & Wi-Fi

Aplicação web em HTML único voltada para técnicos de campo da Claro na leitura rápida de etiquetas de gateways/modens e redes Wi-Fi.

## Funcionalidades

- **4 Campos de Cópia Rápida no Topo**:
  1. **Usuário 192.168.0.1** (com prefixo `CLARO_` ou `NET_` mantendo o `_`).
  2. **Senha 192.168.0.1** (foco em 12 dígitos).
  3. **Usuário Wi-Fi (SSID)** (com prefixo `CLARO_` ou `NET_` mantendo o `_`, priorizando proximidade com `SSID`, `2.4`, `2.4 GHz` e `5GHz`).
  4. **Senha Wi-Fi** (foco em 8 dígitos).
  - Ao tocar/clicar em qualquer um dos 4 campos, o valor é copiado automaticamente para a área de transferência.
- **Captura com Câmera e OCR Forçado**:
  - Suporte à câmera traseira ao vivo (`Abrir Câmera` -> `Capturar & Extrair`) e seleção de imagem (`Foto / Galeria`).
  - Extração forçada para sempre preencher os 4 campos e permitir ajuste manual imediato.
- **Arquivar, Exportar e Importar**:
  - Salva registros localmente no navegador (`localStorage`).
  - Exporta e importa **JSON** e **CSV**, além de exportar **PDF**.

## Rodapé e Versionamento

O rodapé exibe exatamente:
`Criado por: Fernando Sato - Versão 1.1 - 24/11/2026 20:37`

A versão, data e hora são estáticas no HTML e devem ser alteradas apenas quando houver edição de revisão.
