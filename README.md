# Configuração eMTA 192.168.0.1 — Claro Telecom

Ferramenta web em arquivo único (`index.html`) voltada para técnicos de campo da **Claro**, facilitando a leitura de etiquetas de **eMTA / Gateways**, cópia rápida de credenciais e acesso ao painel `http://192.168.0.1`.

## Funcionalidades

1. **4 Campos de Cópia Rápida no Topo (1-Tap Copy)**
   - **1. Usuário 192.168.0.1**: preenchido automaticamente a partir da leitura/edição e copiado ao tocar no campo.
   - **2. Senha 192.168.0.1**: preenchido automaticamente e copiado ao tocar no campo.
   - **3. Usuário Wi-Fi (2.4 GHz ou 5 GHz)**: alternância rápida entre bandas `2.4 GHz` e `5 GHz` para SSIDs iniciados em `CLARO_` ou `NET_`, com cópia ao tocar.
   - **4. Senha Wi-Fi**: preenchido automaticamente e copiado ao tocar no campo.

2. **Captura pela Câmera e Leitura OCR da Etiqueta**
   - Botão **Abrir Câmera** com mira de enquadramento e captura de foto (`Tirar Foto e Ler`), além de opção **Foto / Arquivo** para galeria/arquivos.
   - Extrai e formata na parte inferior da página:
     - **Modelo**
     - **Fabricante**
     - **Input** (alimentação elétrica)
     - **Fabr.**
     - **S/N**
     - **CM MAC**
     - **eMTA MAC**
     - **Usuário e Senha do IP `192.168.0.1`**
     - **SSIDs Wi-Fi 2.4 GHz e 5 GHz (`CLARO_` / `NET_`)** e **Senha Wi-Fi**
   - Inclui área expansível de texto bruto do OCR para conferência ou reprocessamento manual.

3. **Rodapé de Revisão Estático**
   - Exibe: `Criado por: Fernando Sato - Versão 1.1 - 24/11/2026 20:37`.
   - A versão, data e hora no rodapé **não** mudam a cada visualização; são atualizadas apenas quando uma revisão do código é editada.

## Observação de Uso no Navegador (Câmera)
Para que o navegador permita acesso direto à câmera (`getUserMedia`), abra o `index.html` via **HTTPS** (por exemplo, GitHub Pages) ou **localhost**. Caso abra via `file://` em algum navegador restritivo, utilize o botão **Foto / Arquivo**.
