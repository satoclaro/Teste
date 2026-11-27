# eMTA Label Scanner — correções

## O que mudou
- Leitura do campo **Usuário** baseada no rótulo `Usuário:` (mesma linha ou linha seguinte).
- Leitura do campo **Senha** baseada no rótulo `Senha:` (mesma linha ou linha seguinte), preenchindo a senha de acesso do IP.
- Busca sequencial de credenciais após o rótulo `IP: 192.168.0.1` e conferência da ordem IP → Usuário → Senha.
- OCR simplificado para uma passagem por foto e worker reutilizado entre leituras, para acelerar.
- Botão **Abrir câmera** tenta câmera direta; em caso de bloqueio, abre o seletor de captura da câmera do Android.
- Botão **Selecionar foto** permanece disponível como alternativa.

## Como abrir
1. Abra `emta_label_scanner_v2.html` em um navegador atualizado.
2. Para câmera direta, use o site em HTTPS (ou localhost). Navegadores bloqueiam câmera direta em páginas locais `file://` em muitos aparelhos.
3. Se a câmera direta não abrir, **Abrir câmera** aciona o seletor de captura do aparelho; escolha Câmera.
4. Tire/seleciona a foto e toque em **Reconhecer etiqueta (OCR)**.
5. Confira os campos. O OCR pode confundir caracteres visualmente semelhantes, como `B/8` ou `6/8`; não há correção automática desses caracteres para evitar alteração silenciosa. Se estiver incerto, confira na etiqueta.

## Privacidade
OCR é executado no navegador. A biblioteca Tesseract.js é carregada via CDN, então é necessária conexão inicial com a internet. O HTML não envia a foto para um servidor deste projeto.
