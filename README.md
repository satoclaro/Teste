# Leitor de Etiqueta de Modem

Página HTML única (funciona no celular e no computador) que abre a câmera, fotografa a etiqueta do modem e extrai:

1. **Login do IP 192.168.0.1** (começa com `CLARO_` ou `NET_`)
2. **Senha do IP 192.168.0.1** (normalmente 12 caracteres)
3. **Usuário da rede Wi-Fi** (SSID 2.4 GHz)
4. **Senha da rede Wi-Fi** (normalmente 8 caracteres)

Os 4 campos ficam no topo. **Tocar/clicar em qualquer campo copia o valor para a área de transferência.**

Criado por: Fernando Sato

## Como usar

1. Abra `index.html` no navegador (Chrome recomendado). **É necessária internet**, pois o OCR (Tesseract.js), o gerador de PDF (jsPDF) e o leitor de PDF (pdf.js) são carregados por CDN.
2. Toque em **📷 Abrir câmera** (no celular abre a câmera nativa; no PC abre a webcam) ou em **🖼️ Galeria / arquivo**.
3. Aguarde a leitura. Os campos são preenchidos automaticamente.
4. Toque no campo desejado para copiar.
5. Se algum caractere vier errado, edite direto no campo. Se a foto estiver inclinada, use o controle **Girar** e clique em **Reler**.

Dica de foto: só a etiqueta no enquadramento, boa luz, sem reflexo, texto na horizontal e de perto.

## Como a leitura funciona

- A leitura para assim que todas as fontes concordam (login, SSID, senha do IP, senha Wi-Fi e CM MAC). Se houver divergência, faz até 5 leituras e vota **caractere a caractere**, usando o fato de o mesmo final (ex.: `3430B5`) aparecer em várias partes da etiqueta. Isso evita confundir `B` com `8` e `6` com `8`.
- Se o login não for encontrado, a foto é girada automaticamente (90°, 270°, 180°) e relida.
- O login é o texto `CLARO_xxxxxx` / `NET_xxxxxx` logo após "Usuário"/"Login"; o SSID é o que vem após "SSID", "2.4GHz" etc. (`CLARO_2G…`, `NET_2G…`).
- Senhas: aceita as que vêm após "Senha". Prefere 12 caracteres (IP) e 8 caracteres (Wi-Fi), mas também reconhece etiquetas novas com senhas aleatórias de outro tamanho (ex.: 15/16 e 10 caracteres).
- Correções automáticas: confusões `O/0`, `I/1`, `S/5` em trechos hexadecimais e conferência com o final do usuário (ex.: `CLARO_3430B5` → senhas terminam em `3430B5`).
- Se a senha Wi-Fi não for lida mas a senha do IP tiver 12 caracteres, a senha Wi-Fi é deduzida dos **últimos 8 dígitos** da senha do IP (padrão desses modems). A página avisa quando isso acontece.
- Em "Texto bruto lido" você vê o que o OCR enxergou, útil para diagnóstico.

## Arquivo, exportar e importar

- **💾 Arquivar**: salva os 4 campos no arquivo local (armazenado no navegador do aparelho, via `localStorage`).
- **Exportar**: CSV, JSON ou PDF.
- **Importar**: CSV, JSON ou PDF. O PDF precisa ter sido gerado por esta página (formato próprio). Registros repetidos são ignorados.
- Busca, carregar registro nos campos, excluir um registro e apagar tudo.

## Versão do rodapé

O rodapé é montado a partir da constante `BUILD` no HTML (`versao`, `data`, `hora`). Ele **não usa a data/hora de quem abre a página**: só muda quando o arquivo é revisado, e a cada alteração a versão, a data e a hora são atualizadas.

Histórico:
- 1.1 - 24/11/2026 20:37 - versão inicial
- 1.2 - 26/11/2026 22:43 - rodapé atualizado por revisão; votação caractere a caractere (B/8, 6/8); leitura mais rápida

## Privacidade e cuidados

- A leitura da foto é feita **no próprio aparelho**; a imagem não é enviada para servidor (só as bibliotecas são baixadas dos CDNs).
- Os registros arquivados contêm senhas em texto puro no armazenamento do navegador e nos arquivos exportados. Use apenas em equipamento autorizado, guarde/compartilhe os arquivos com cuidado e apague registros que não precisar mais.
- Use somente em equipamentos sob sua responsabilidade de atendimento.

## Limitações

- Fotos desfocadas, com reflexo ou muito inclinadas podem gerar leitura errada: confira os campos antes de usar.
- O OCR precisa de internet na primeira leitura para baixar o motor e o idioma.
