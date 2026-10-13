# Clube Torra Mirante — landing page

Projeto de estudo e portfólio: landing page de assinatura de café especial.
A marca, os preços e os depoimentos são fictícios.

## O que tem nesta pasta

```
torra-mirante/
├── index.html      ← a página inteira (HTML, CSS e JavaScript num só arquivo)
├── img/            ← fotos usadas na página
│   └── og-image.jpg  ← imagem que aparece quando o link é compartilhado
├── fonts/          ← fontes hospedadas no próprio site, com as licenças
└── LEIA-ME.md      ← este guia
```

## Segurança e privacidade

- **Nenhum dado é guardado ou enviado.** O e-mail do cupom só é conferido no navegador.
- **Nenhuma conexão com terceiros ao abrir a página.** Fontes e imagens vêm do próprio site.
- **Política de segurança (CSP)** no `<head>`: o navegador só aceita arquivos do próprio site e bloqueia envio de dados para fora. Se um dia você adicionar Google Analytics, um formulário real ou fontes de outro lugar, precisa liberar o endereço novo nessa linha, senão ele será bloqueado.
- As fontes (DM Serif Display, Manrope e Caveat) usam a licença livre SIL Open Font License; os arquivos de licença estão na pasta `fonts/`.

O nome `index.html` é importante: é o arquivo que o servidor abre quando alguém acessa o endereço do site.

## Antes de publicar: teste no seu computador

1. Descompacte o .zip.
2. Dê dois cliques em `index.html`. A página abre no navegador.
3. Clique nos botões, troque formato e frequência, teste o cupom.

Se tudo funciona aqui, vai funcionar publicado.

---

## Opção 1 — Netlify Drop (mais rápida, 2 minutos)

Boa para ver o site no ar logo de cara.

1. Acesse **app.netlify.com/drop**.
2. Arraste a **pasta** `torra-mirante` inteira (não o .zip) para a área indicada.
3. Em segundos, o Netlify mostra um link do tipo `https://nome-aleatorio.netlify.app`.
4. Para o link não expirar e poder mudar o nome, crie uma conta grátis quando o Netlify pedir.
   Depois, em **Site configuration → Change site name**, troque para algo como `torra-mirante`.

## Opção 2 — GitHub Pages (recomendada para portfólio)

Além de publicar, deixa o código visível no seu GitHub, o que conta pontos com recrutadores.

1. Crie uma conta grátis em **github.com** (se ainda não tiver).
2. Clique em **+ → New repository**.
   - Nome: `torra-mirante`
   - Marque **Public**
   - Clique em **Create repository**.
3. Na página do repositório, clique em **uploading an existing file**.
4. Arraste para lá o `index.html`, o `LEIA-ME.md` e as pastas `img` e `fonts` inteiras.
5. Lá embaixo, clique em **Commit changes**.
6. Vá em **Settings → Pages**.
   - Em **Source**, escolha **Deploy from a branch**.
   - Em **Branch**, escolha **main** e a pasta **/ (root)**. Clique em **Save**.
7. Espere 1 ou 2 minutos e atualize a página. Vai aparecer o endereço:
   `https://SEU-USUARIO.github.io/torra-mirante/`

Os nomes dos menus podem mudar um pouco com o tempo, mas o caminho é sempre: criar repositório → enviar arquivos → ativar o Pages.

## Depois de publicar

### 1. Ajuste o link de compartilhamento
Abra `index.html` e procure `SEU-ENDERECO` (aparece 2 vezes, nas linhas de `og:image` e `og:url`).
Troque pelo endereço real do site, sem barra no final. Exemplo:

```html
<meta property="og:image" content="https://seu-usuario.github.io/torra-mirante/img/og-image.jpg">
<meta property="og:url" content="https://seu-usuario.github.io/torra-mirante/">
```

Envie o arquivo de novo. Agora, ao colar o link no WhatsApp ou LinkedIn, aparece a foto e o título.
Para conferir, use o **Sharing Debugger** do Facebook (developers.facebook.com/tools/debug).

### 2. Como atualizar o site
- **GitHub:** no repositório, clique em `index.html` → ícone de lápis → edite → **Commit changes**. Ou envie o arquivo novo por cima pelo **Add file → Upload files**. O site atualiza em 1 ou 2 minutos.
- **Netlify:** em **Deploys**, arraste a pasta atualizada de novo.

### 3. Teste no celular
Abra o link no seu celular. Confira a barra "Assinar" que aparece ao rolar e o botão do WhatsApp.

## Próximos passos de estudo

- **Domínio próprio:** registrar um `.com.br` no registro.br e apontar para o GitHub Pages ou Netlify.
- **Separar arquivos:** mover o CSS para `style.css` e o JavaScript para `script.js`. É a organização usada em projetos maiores.
- **Medir visitas:** instalar o Google Analytics e ver de onde vêm os acessos.
- **Desempenho:** rodar o **PageSpeed Insights** (pagespeed.web.dev) com o seu link e ver as notas de velocidade e acessibilidade.
- **Git de verdade:** aprender a publicar pelo terminal com `git add`, `git commit` e `git push`, em vez de enviar pelo site.

## Para o portfólio

Ao apresentar o projeto, conte as decisões, não só o resultado:
- Começou como home de loja e virou landing page de um objetivo só (assinatura).
- Seletor de formato, frequência e quantidade com preço por xícara calculado na hora.
- Testada em computador e celular: sem rolagem lateral, áreas de toque de 44 px, contraste adequado e navegação por teclado.
