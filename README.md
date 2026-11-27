# Leitor de Etiquetas Telecom — v1.1

Página HTML local para fotografar/selecionar uma etiqueta de modem, executar OCR e organizar os quatro campos:

1. Usuário do IP `192.168.0.1`
2. Senha do IP `192.168.0.1`
3. Usuário da rede Wi-Fi
4. Senha da rede Wi-Fi

## Como usar
1. Extraia o ZIP e abra `index.html` no navegador (Chrome/Edge recomendados).
2. Clique **Abrir câmera** para fotografar ou **Selecionar foto** para carregar uma imagem.
3. Clique **Extrair informações**. A leitura OCR usa Tesseract.js via CDN, portanto precisa de internet na primeira execução/para carregar a biblioteca.
4. Confira e corrija os campos. OCR pode trocar letras/números e o layout das etiquetas varia.
5. Clique/toque em qualquer campo para copiar o conteúdo automaticamente.
6. **Arquivar registro** guarda o conteúdo localmente no navegador.
7. CSV/JSON exportam os campos preenchidos no formulário. Importação CSV/JSON permite restaurar registros. PDF/Imprimir abre a impressão do navegador (selecione “Salvar como PDF”).

## Privacidade e segurança
- Os registros ficam no `localStorage` do navegador neste aparelho/perfil, não em um servidor.
- Credenciais são informações sensíveis: não exporte, compartilhe nem deixe arquivos de backup acessíveis a terceiros.
- O botão PDF/Imprimir gera uma página de impressão; escolha “Salvar como PDF” no diálogo.
- Se o OCR falhar, digite/corrija os campos manualmente. O app não valida credenciais no modem.

## Limitações do OCR
As regras de extração tentam reconhecer usuários que começam com `CLARO_` ou `NET_`, senhas de 12 dígitos do acesso ao modem e senhas Wi-Fi de 8 dígitos. A leitura pode confundir caracteres semelhantes; revise antes de copiar ou arquivar.

## Versão
Rodapé fixo no HTML: **Criado por: Fernando Sato - Versão 1.1 - 24/11/2026 20:37**. O texto não é atualizado automaticamente em cada visualização.
