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

## Solução: Função Câmera Não Funciona (eMTA e ONT Claro)

Quando o botão **Abrir Câmera** não abre o vídeo ao vivo no navegador ou aplicativo:

1. **Contexto Seguro (HTTPS)**: navegadores bloqueiam `navigator.mediaDevices.getUserMedia` em páginas abertas fora de `HTTPS` ou `localhost` (por exemplo, arquivos locais `file://` ou URLs `http://` externas). Hospede o arquivo em **HTTPS** (como GitHub Pages) para ativar a câmera ao vivo.
2. **Permissão do Navegador / App**: verifique nas configurações do navegador (ex.: Chrome no Android) se a permissão de **Câmera** está permitida para o site. Se o aplicativo estiver rodando dentro de uma *WebView* sem permissão de câmera habilitada no app, a câmera direta pode falhar.
3. **Fallback Automático pela Câmera Nativa do Sistema (`Foto / Arquivo`)**: caso a câmera direta não abra ou falhe, o código aciona automaticamente o seletor `<input type="file" accept="image/*" capture="environment">`, permitindo tirar a foto pela câmera padrão do aparelho ou escolher uma imagem salva e executar o OCR normalmente.

## Uso no Chrome no Android via GitHub Pages

1. **Verifique a URL HTTPS**: acesse pelo endereço `https://<usuario>.github.io/<repositorio>/` (não abra o arquivo cru `blob/...` no GitHub, pois o GitHub serve páginas brutas com cabeçalhos que podem bloquear recursos ou scripts).
2. **Permissão de Câmera no Chrome**:
   - Ao tocar em **Abrir Câmera**, toque em **Permitir** no aviso do Chrome.
   - Se já estiver bloqueado, toque no ícone de configurações/cadeado ao lado da URL → **Permissões** → **Câmera** → **Permitir** (ou em **Configurações do Android → Apps → Chrome → Permissões → Câmera**).
3. **Câmera ocupada ou fallback automático**: se outro aplicativo estiver usando a câmera ou o Chrome bloquear o stream ao vivo, a página exibe o motivo exato na barra de status e abre automaticamente a câmera nativa / galeria para tirar a foto e rodar o OCR.
