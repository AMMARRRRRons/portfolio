# Guide EmailJS - Configuration Complète

## ⚡ Configuration en 5 minutes

### ÉTAPE 1 : Créer un compte EmailJS (1 minute)

1. Allez sur **https://www.emailjs.com/**
2. Cliquez sur **"Sign Up"** (en haut à droite)
3. Inscrivez-vous avec :
   - Votre email : `ons.ammar@edu.univ-paris13.fr`
   - Un mot de passe
   - Cliquez sur **"Sign Up"**
4. Vérifiez votre email (cliquez sur le lien dans l'email reçu)

---

### ÉTAPE 2 : Ajouter un service email (2 minutes)

1. Une fois connecté, dans le dashboard, cliquez sur **"Email Services"** (menu de gauche)
2. Cliquez sur **"Add New Service"**
3. Choisissez **"Gmail"** (ou votre fournisseur d'email)
4. Cliquez sur **"Connect Account"**
5. Connectez-vous avec votre compte Gmail (ons.ammar@edu.univ-paris13.fr)
6. Autorisez EmailJS à envoyer des emails
7. **IMPORTANT** : Notez le **Service ID** qui apparaît (ex: `service_abc123`)
   - Il ressemble à : `service_xxxxxxxxx`
   - **Copiez-le, vous en aurez besoin !**

---

### ÉTAPE 3 : Créer un template email (1 minute)

1. Dans le menu de gauche, cliquez sur **"Email Templates"**
2. Cliquez sur **"Create New Template"**
3. Donnez un nom : `Portfolio Contact`
4. Dans le template, remplacez tout par :

```
Sujet: {{subject}}

Message:
{{message}}

De: {{from_name}} ({{from_email}})
```

5. Dans le champ **"To Email"**, mettez : `{{to_email}}`
6. Dans le champ **"From Name"**, mettez : `{{from_name}}`
7. Cliquez sur **"Save"**
8. **IMPORTANT** : Notez le **Template ID** qui apparaît (ex: `template_xyz789`)
   - Il ressemble à : `template_xxxxxxxxx`
   - **Copiez-le, vous en aurez besoin !**

---

### ÉTAPE 4 : Obtenir votre Public Key (30 secondes)

1. Dans le menu de gauche, cliquez sur **"Account"**
2. Cliquez sur **"General"**
3. Trouvez la section **"API Keys"**
4. **IMPORTANT** : Copiez votre **Public Key**
   - Il ressemble à : `abcdefghijklmnop` (une longue chaîne de lettres)
   - **Copiez-le, vous en aurez besoin !**

---

### ÉTAPE 5 : Mettre à jour le fichier script.js (30 secondes)

1. Ouvrez le fichier `assets/js/script.js`
2. Trouvez les lignes 45-47 (elles contiennent actuellement des valeurs par défaut)
3. Remplacez par vos vraies valeurs :

```javascript
const EMAILJS_SERVICE_ID = 'VOTRE_SERVICE_ID_ICI';      // Ex: service_abc123
const EMAILJS_TEMPLATE_ID = 'VOTRE_TEMPLATE_ID_ICI';    // Ex: template_xyz789
const EMAILJS_PUBLIC_KEY = 'VOTRE_PUBLIC_KEY_ICI';      // Ex: abcdefghijklmnop
```

**Exemple concret :**
```javascript
const EMAILJS_SERVICE_ID = 'service_gmail123';
const EMAILJS_TEMPLATE_ID = 'template_portfolio456';
const EMAILJS_PUBLIC_KEY = 'abcdefghijklmnopqrstuvwxyz';
```

4. **Sauvegardez le fichier**

---

## ✅ Test

1. Ouvrez votre site dans le navigateur
2. Allez à la section Contact
3. Remplissez le formulaire avec :
   - Nom : Test
   - Email : test@example.com
   - Message : Test EmailJS
4. Cliquez sur "Envoyer le message"
5. Vous devriez voir : "Merci pour votre message ! Il a été envoyé."
6. Vérifiez votre boîte mail `ons.ammar@edu.univ-paris13.fr`
7. Vous devriez recevoir un email avec le format : "Test, test@example.com, Test EmailJS"

---

## 🎉 C'est terminé !

Le formulaire fonctionne maintenant. Les visiteurs peuvent envoyer des messages et vous les recevrez directement sur votre boîte mail sans qu'ils soient redirigés.

---

## ❓ Problèmes courants

**"EmailJS n'est pas chargé"**
- Vérifiez votre connexion internet
- Vérifiez que le script EmailJS est bien chargé dans index.html

**"Service ID invalide"**
- Vérifiez que vous avez bien copié le Service ID depuis EmailJS
- Il doit commencer par `service_`

**"Template ID invalide"**
- Vérifiez que vous avez bien copié le Template ID depuis EmailJS
- Il doit commencer par `template_`

**"Public Key invalide"**
- Vérifiez que vous avez bien copié la Public Key depuis EmailJS
- C'est une longue chaîne de lettres (pas de chiffres)

**L'email n'arrive pas**
- Vérifiez votre boîte spam
- Vérifiez que le service email est bien connecté dans EmailJS
- Vérifiez les logs dans la console du navigateur (F12)

