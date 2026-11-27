# Leitor de Etiquetas Telecom — v1.2

HTML local para capturar uma etiqueta de modem, extrair texto com OCR e preencher quatro campos:

1. Usuário do IP `192.168.0.1`
2. Senha do IP `192.168.0.1`
3. Usuário da rede Wi-Fi
4. Senha da rede Wi-Fi

## Melhorias na v1.2
- O login do modem é buscado pelo contexto do endereço `192.168.0.1` e pelo rótulo `Usuário`.
- A senha do modem é buscada após o rótulo `Senha`, priorizando o valor alfanumérico de 12 caracteres.
- Usuário Wi-Fi identificado pelo contexto de `SSID`, `2.4 GHz` ou `5 GHz`, priorizando `CLARO_` e `NET_`.
- Senha Wi-Fi é procurada junto ao contexto Wi-Fi e rótulo `Senha`, com 8 caracteres.
- Não aplica substituições automáticas entre `B` e `8` ou entre `6` e `8`, para evitar alterar credenciais reais.
- Botão **Abrir câmera** solicita acesso à câmera diretamente no navegador e apresenta uma tela de captura; se não funcionar, abre o seletor de fotos como alternativa.
- OCR usa um worker reutilizável, evitando reinicializar o motor a cada leitura.

## Como usar
1. Extraia o ZIP e abra `index.html` no Chrome ou navegador compatível.
2. Toque em **Abrir câmera** e permita o acesso; ou use **Selecionar foto**.
3. Capture/carregue a etiqueta e toque em **Extrair informações**.
4. Confira os quatro campos. OCR pode confundir caracteres, principalmente em fotos desfocadas.
5. Toque em cada campo para copiar o conteúdo.
6. Use **Arquivar registro**, exportação CSV/JSON ou PDF/Imprimir. Os botões de importação aceitam CSV e JSON.

## Privacidade
- O arquivo de registros é salvo no `localStorage` do navegador/aparelho, não em servidor.
- Arquivos CSV/JSON e PDF podem conter credenciais: mantenha-os protegidos.
- O leitor não testa as credenciais no equipamento.

## Limitações
- OCR depende da biblioteca Tesseract.js carregada por CDN, portanto é necessária conexão à internet para carregar o mecanismo.
- O acesso à câmera depende de permissões do navegador e, em alguns ambientes, de contexto seguro (HTTPS ou localhost). Se o botão não conseguir abrir, use **Selecionar foto**.
- OCR não pode garantir distinção perfeita de caracteres visualmente semelhantes. Não substitui a conferência manual.

## Versão e revisão
Rodapé fixo desta revisão: **Criado por: Fernando Sato - Versão 1.2 - 26/11/2026 22:18**. A data/hora é um carimbo estático da revisão e só muda quando o arquivo é atualizado para uma nova versão; não muda ao visualizar/abrir a página.
