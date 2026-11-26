# Configuração eMTA / ONT 192.168.0.1 — Claro / NET

Ferramenta web em arquivo único (`index.html`) baseada em **captura de foto em alta resolução** com extração OCR multi-passagem e reconstrução de traços finos (`_`):
- **Captura de foto**: câmera web em alta resolução ou câmera nativa (`Tirar Foto Direto`), com pré-processamento de escala 2.0x–2.1x e limiar suave para não perder o caractere `_` (underline).
- **Extração reforçada de credenciais**:
  - **Usuário `192.168.0.1`**: captura valores logo abaixo de `192.168.0.1` e após o rótulo `Usuário`, inclusive quando começam com `CLARO_` (restaurando automaticamente o `_` caso o OCR leia espaço ou hífen).
  - **Senha `192.168.0.1`**
  - **Redes Wi-Fi começando com `CLARO_` ou `NET_`** (2.4 GHz e 5 GHz com `_`) e **Senha Wi-Fi**
  - **DOCSIS**, Modelo, Fabricante, Input, Fabr., S/N, CM MAC e eMTA MAC
- **4 campos de cópia rápida no topo**, arquivamento local e exportação/importação em CSV, JSON e PDF.
- **Rodapé estático**: `Criado por: Fernando Sato - Versão 1.2 - 26/11/2026 20:30`.
