# Configuration Formspree pour le formulaire de contact

## Étapes rapides (2 minutes)

1. **Créer un compte Formspree** (gratuit)
   - Allez sur https://formspree.io/
   - Créez un compte gratuit (1000 soumissions/mois gratuites)

2. **Créer un nouveau formulaire**
   - Dans le dashboard, cliquez sur "New Form"
   - Donnez un nom (ex: "Portfolio Contact")
   - Dans "Email to", mettez: `ons.ammar@edu.univ-paris13.fr`
   - Cliquez sur "Create Form"

3. **Obtenir votre Form ID**
   - Une fois le formulaire créé, vous verrez votre Form ID
   - Il ressemble à: `xrgkqyvw` ou `abc123def`

4. **Mettre à jour le fichier script.js**
   - Ouvrez `assets/js/script.js`
   - À la ligne 42, remplacez `YOUR_FORM_ID` par votre Form ID :
     ```javascript
     const FORMSPREE_ENDPOINT = 'https://formspree.io/f/VOTRE_FORM_ID';
     ```

## C'est tout !

Le formulaire enverra maintenant les emails directement à `ons.ammar@edu.univ-paris13.fr` avec le format :
```
Nom, Email, Message
```

Le visiteur ne sera **PAS** redirigé vers sa boîte mail.

## Format des emails reçus

Vous recevrez un email avec :
- **Sujet**: Contact portfolio - [Nom du visiteur]
- **Corps**: Nom, Email, Message (format demandé)

