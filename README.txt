Sabor da Sopa — Padrão PRODUTOS (migração do seu banco)

Arquivos:
- index.html  -> Cliente
- admin.html  -> Admin (Firebase Auth)
- migrar.html -> Migração menuItems -> produtos
- firebase-config.js
- firestore.rules.txt

PASSO A PASSO (recomendado):
1) No Firebase > Firestore > Rules:
   - cole o conteúdo de firestore.rules.txt e PUBLIQUE

2) Suba todos os arquivos no GitHub Pages (mesma pasta):
   - index.html, admin.html, migrar.html, firebase-config.js

3) Faça a migração:
   - Abra: https://SEUUSUARIO.github.io/SEUREPO/migrar.html
   - Faça login com um admin
   - Clique "Migrar agora"
   - Isso cria a coleção "produtos" com os campos: cat, nome, preco, ord, imageUrl, desc

4) Depois disso:
   - Seu sistema (index/admin) usa a coleção "produtos".

Observação:
- menuItems fica protegido (apenas admin) pelas rules deste pacote.
