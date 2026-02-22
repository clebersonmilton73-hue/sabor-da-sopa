Sabor da Sopa — Segurança REAL (Firebase) + Admin separado

📌 Arquivos:
- index.html  -> CLIENTE (cardápio + checkout + envia Whats do cliente)
- admin.html  -> ADMIN (login email/senha Firebase + bloqueio 3 tentativas)
- firebase-config.js -> COLE o firebaseConfig + defina ADMIN_EMAIL
- firestore.rules.txt -> regras recomendadas para segurança real
- .htaccess.sample -> proteção extra (só Apache)

✅ PASSO A PASSO (Firebase):
1) Crie projeto no Firebase Console.
2) Authentication > Sign-in method:
   - ative "Email/Password"
   - crie o usuário admin (seu email) em Authentication > Users
3) Firestore Database:
   - crie em "Production mode"
   - abra "Rules" e cole o conteúdo de firestore.rules.txt
   - troque SEU_EMAIL_ADMIN@exemplo.com pelo seu email
4) Project settings > Your apps (Web) > pegue o firebaseConfig
   - cole dentro do arquivo firebase-config.js
   - ajuste ADMIN_EMAIL pro seu email admin

✅ PASSO A PASSO (GitHub Pages):
- Suba os 2 arquivos + firebase-config.js
- Acesse:
  - /index.html (cliente)
  - /admin.html (admin)

🛡️ Bloqueio 3 tentativas:
- após 3 tentativas erradas, trava 15 minutos (neste navegador)

🔑 “Senha criptografada”:
- No Firebase Auth, a senha NÃO fica no seu arquivo. O Firebase guarda com hash seguro no servidor.

🔒 .htaccess:
- Só para Apache. No GitHub Pages NÃO funciona.
