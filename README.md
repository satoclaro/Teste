# Config EMTA – 192.168.0.1

Página HTML de apoio para o técnico de campo: tira foto da etiqueta do EMTA, lê as informações (OCR) e deixa **usuário/senha do 192.168.0.1** e **SSID/senha do Wi-Fi** prontos para copiar com um toque.

## Como usar

1. Copie a pasta (ou só o `index.html`) para o celular/notebook e abra no navegador (Chrome recomendado).
   - Pode também hospedar em qualquer servidor interno **https**; funciona igualmente.
2. Toque em **📷 Tirar foto da etiqueta**. No celular abre a câmera traseira; no computador abre o seletor de arquivos. Há também o botão **Galeria**.
3. Aguarde a leitura. Os dados aparecem em **Informações extraídas** (fim da página) e os 4 campos do topo são preenchidos sozinhos.
4. Toque em qualquer campo do topo para **copiar automaticamente** para a área de transferência (aparece "Copiado!"):

   | Campo | Conteúdo |
   |-------|----------|
   | 1 | Usuário do IP 192.168.0.1 |
   | 2 | Senha do IP 192.168.0.1 |
   | 3 | Usuário (SSID) da rede Wi-Fi |
   | 4 | Senha da rede Wi-Fi |

5. Os botões **2.4 GHz / 5 GHz** abaixo dos campos escolhem qual rede aparece nos campos 3 e 4.
6. Use **Abrir 192.168.0.1** para ir à página do equipamento e cole os dados nos campos de login.

> O navegador não permite que uma página preencha o login de outro endereço (192.168.0.1). Por isso a página copia os valores e você cola no login do modem.

## Informações extraídas

Fabricante, Modelo, Input, Fabr., S/N, CM MAC, EMTA MAC, usuário e senha do 192.168.0.1, SSID e senha Wi-Fi 2.4 GHz e 5 GHz (SSIDs que começam com `CLARO_` ou `NET_`).

- Todos os campos da seção **Informações extraídas** são editáveis: corrija erros do OCR ali e o topo da página acompanha.
- Cada campo tem um botão ⧉ para copiar; **Copiar tudo** copia o resumo formatado; **Limpar** zera tudo.
- O bloco *Texto bruto lido pelo OCR* ajuda a ver o que o leitor enxergou.

## Requisitos e privacidade

- O OCR usa [Tesseract.js](https://github.com/naptha/tesseract.js), carregado de CDN. **Precisa de internet na primeira leitura**; depois o navegador guarda os arquivos em cache.
- A foto é processada **no próprio aparelho**: a imagem não é enviada a nenhum servidor.
- Nada é salvo: ao fechar ou recarregar a página, os dados somem.

## Dicas para uma boa leitura

- Boa iluminação, sem reflexo/flash sobre a etiqueta.
- Câmera paralela à etiqueta, texto nítido e ocupando a maior parte da foto.
- Confira sempre caracteres parecidos: `0/O`, `1/I/L`, `5/S`, `8/B`.
- Se a etiqueta tiver uma única senha Wi-Fi para as duas bandas, ela é aplicada às duas (a página avisa para você conferir).

## Atualizar versão, data e hora (rodapé)

O rodapé é **texto fixo**: não muda a cada visualização. Só altere quando revisar o arquivo. Procure no `index.html` a linha abaixo e edite versão, data e hora:

```html
<footer>Criado por: Fernando Sato - Versão 1.1 - 24/11/2026 20:37</footer>
```

Exemplo após uma revisão: `Versão 1.2 - 25/11/2026 09:10`.

## Arquivos

- `index.html` – aplicação completa (HTML + CSS + JS em um arquivo)
- `README.md` – este guia
