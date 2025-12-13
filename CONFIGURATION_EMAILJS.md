# Configuration EmailJS (2 minutes - GRATUIT)

## Pourquoi EmailJS ?
EmailJS est plus fiable que FormSubmit et fonctionne immédiatement après configuration.

## Étapes rapides :

1. **Créer un compte** (gratuit - 200 emails/mois)
   - Allez sur https://www.emailjs.com/
   - Cliquez sur "Sign Up" et créez un compte

2. **Ajouter un service email**
   - Dans le dashboard, cliquez sur "Email Services"
   - Cliquez sur "Add New Service"
   - Choisissez "Gmail" (ou votre fournisseur)
   - Connectez votre compte Gmail (ons.ammar@edu.univ-paris13.fr)
   - Notez le **Service ID** (ex: `service_abc123`)

3. **Créer un template**
   - Allez dans "Email Templates"
   - Cliquez sur "Create New Template"
   - Utilisez ce template :
   
   ```
   Sujet: {{subject}}
   
   Message:
   {{message}}
   
   De: {{from_name}} ({{from_email}})
   ```
   
   - Dans "To Email", mettez: `{{to_email}}`
   - Notez le **Template ID** (ex: `template_xyz789`)

4. **Obtenir votre Public Key**
   - Allez dans "Account" > "General"
   - Copiez votre **Public Key** (ex: `abcdefghijklmnop`)

5. **Mettre à jour script.js**
   - Ouvrez `assets/js/script.js`
   - Lignes 43-45, remplacez :
     ```javascript
     const EMAILJS_SERVICE_ID = 'VOTRE_SERVICE_ID';
     const EMAILJS_TEMPLATE_ID = 'VOTRE_TEMPLATE_ID';
     const EMAILJS_PUBLIC_KEY = 'VOTRE_PUBLIC_KEY';
     ```

## C'est tout ! Le formulaire fonctionnera immédiatement.

