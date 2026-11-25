# eMTA Label Scanner — Upgrade v2

Scanner responsivo de etiquetas eMTA para uso em campo.

## Melhorias
- Interface escura com acabamento mais moderno e adaptada a celular.
- Captura por câmera e seleção de imagem.
- OCR com duas passagens (imagem original e contraste/limiarização), selecionando o resultado com mais texto.
- Campos de modelo, fabricante, input, fabricação, serial, CM MAC, eMTA MAC, IP, SSID e usuário quando encontrados.
- Resumo final formatado e botão copiar.
- Campos de senha de administrador e Wi-Fi ficam visíveis na tela e no resumo; devem ser preenchidos manualmente após conferir a etiqueta.

## Uso
1. Abra `index.html` em navegador com permissão de câmera (em alguns navegadores, câmera exige HTTPS ou localhost).
2. Fotografe a etiqueta ou selecione imagem.
3. Clique em **Reconhecer etiqueta (OCR)**.
4. Confira e corrija os dados detectados e preencha os campos de senha manualmente.
5. Copie o resumo final.

O OCR é executado no navegador usando Tesseract.js carregado via CDN; a biblioteca exige internet para carregar. O projeto não persiste os dados capturados.
