# 📧 Créer le Template EmailJS - Instructions Détaillées

## ⚠️ IMPORTANT : Ne choisissez PAS un template prédéfini !

Créez un **nouveau template personnalisé** pour avoir le format exact : "Nom, Email, Message"

---

## Étapes pour créer le template :

### 1. Dans EmailJS Dashboard
- Allez dans **"Email Templates"** (menu de gauche)
- Cliquez sur **"Create New Template"** (bouton en haut à droite)
- **NE cliquez PAS sur les templates prédéfinis** (Contact Us, Auto-Reply, etc.)

### 2. Configuration du template

**Nom du template :**
```
Portfolio Contact
```

**Sujet de l'email :**
```
{{subject}}
```

**Contenu du template :**
Remplacez TOUT le contenu par défaut par ceci :

```
{{message}}

---
De: {{from_name}}
Email: {{from_email}}
```

### 3. Configuration des champs

**To Email :**
```
{{to_email}}
```

**From Name :**
```
{{from_name}}
```

**From Email :**
```
{{from_email}}
```

### 4. Sauvegarder

- Cliquez sur **"Save"** (en haut à droite)
- **IMPORTANT** : Notez le **Template ID** qui apparaît
  - Il ressemble à : `template_xxxxxxxxx`
  - **Copiez-le !**

---

## ✅ Résultat attendu

Quand quelqu'un envoie un message avec :
- Nom : "Ons"
- Email : "onsammar45@gmail.com"  
- Message : "rappelez moi"

Vous recevrez un email avec :
- **Sujet** : "Contact portfolio - Ons"
- **Corps** : 
```
Ons, onsammar45@gmail.com, rappelez moi

---
De: Ons
Email: onsammar45@gmail.com
```

---

## 🎯 Prochaine étape

Une fois le Template ID obtenu, mettez à jour `assets/js/script.js` :

```javascript
const EMAILJS_SERVICE_ID = 'service_rwbacqf';        // ✅ Déjà fait
const EMAILJS_TEMPLATE_ID = 'template_XXXXXXXXX';   // ⬅️ Remplacez par votre Template ID
const EMAILJS_PUBLIC_KEY = 'YOUR_PUBLIC_KEY';        // ⬅️ À obtenir dans Account > General
```

