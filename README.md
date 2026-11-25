# Leitor de etiqueta eMTA (HTML)

Ferramenta de página única para técnicos autorizados, com captura por câmera ou seleção de foto e OCR no navegador para auxiliar na leitura de etiquetas de eMTA.


## Como usar
1. Extraia o ZIP.
2. Abra `index.html` no navegador (para câmera, pode ser necessário servir a página em HTTPS ou `localhost`; permissões de câmera são bloqueadas em muitos contextos de arquivo local).
3. Toque em **Abrir câmera** e autorize a câmera, ou em **Selecionar foto**.
4. Tire/carregue uma foto nítida e toque **Reconhecer etiqueta (OCR)**.
5. Revise e corrija o texto e os campos extraídos.
6. Digite manualmente as senhas nos campos, após confirmar que tem autorização para consultar os dados.
7. Copie o resumo formatado, se necessário.


## O que tenta reconhecer
- Modelo, fabricante, input, FABR, S/N
- CM MAC e eMTA MAC
- IP de acesso
- SSIDs que começam por `CLARO_` ou `NET_` (a identificação de 2.4/5 GHz é heurística; revise)
- Usuário de acesso quando estiver impresso em texto legível


## Privacidade e limitações
- O OCR é executado no dispositivo/navegador usando Tesseract.js, carregado de CDN; é necessária conexão à internet para carregar a biblioteca.
- A foto e os campos não são enviados nem persistidos por este projeto; ficam na página aberta. Evite capturar etiquetas de clientes sem autorização.
- **Senhas não são extraídas automaticamente.** Preencha manualmente os campos de senha após conferir a etiqueta e seguir os procedimentos autorizados.
- O reconhecimento pode confundir caracteres (0/O, 1/I, 5/S, MACs, serial e SSIDs). Sempre valide visualmente.
- O botão de câmera depende de navegador compatível, permissão e HTTPS/localhost.


## Segurança
- Feche a página quando terminar. Não compartilhe capturas, resumo ou credenciais sem autorização.
- Não use em lote para coletar credenciais.


## Tecnologias
- HTML, CSS e JavaScript
- Tesseract.js 5 (CDN)
