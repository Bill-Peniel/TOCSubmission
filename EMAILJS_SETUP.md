# Configuration EmailJS - Instructions

## 🚀 Solution Email Alternative Implémentée !

Votre formulaire utilise maintenant **3 méthodes de fallback** pour envoyer les emails :

### 1. **EmailJS** (Méthode principale)
- ✅ Gratuit jusqu'à 200 emails/mois
- ✅ Très fiable
- ✅ Pas de problème CSRF

### 2. **Netlify Forms** (Fallback 1)
- ✅ Fonctionne si vous hébergez sur Netlify
- ✅ Gratuit jusqu'à 100 soumissions/mois

### 3. **Email Manuel** (Fallback 2)
- ✅ Génère automatiquement l'email
- ✅ Copie dans le presse-papiers
- ✅ Ouvre votre client email

---

## 📋 Configuration EmailJS (Recommandé)

### Étape 1 : Créer un compte EmailJS
1. Allez sur [emailjs.com](https://www.emailjs.com/)
2. Créez un compte gratuit
3. Vérifiez votre email

### Étape 2 : Configurer le service email
1. Dans le dashboard, allez dans **"Email Services"**
2. Cliquez **"Add New Service"**
3. Choisissez votre fournisseur email (Gmail, Outlook, etc.)
4. Suivez les instructions pour connecter votre compte
5. Notez le **Service ID** (ex: `service_xxxxxxx`)

### Étape 3 : Créer un template
1. Allez dans **"Email Templates"**
2. Cliquez **"Create New Template"**
3. Utilisez ce template :

```
Subject: Nouvelle soumission Tower of Challenge

Bonjour,

Vous avez reçu une nouvelle soumission pour Tower of Challenge :

Développeur: {{developerName}}
Email: {{email}}
Nom du jeu: {{gameName}}
Difficulté: {{difficulty}}
Genre: {{genre}}

Description:
{{description}}

Instructions spéciales:
{{instructions}}

Fichiers joints: {{fileCount}} fichiers
- {{fileNames}}

Cordialement,
Tower of Challenge
```

4. Notez le **Template ID** (ex: `template_xxxxxxx`)

### Étape 4 : Obtenir la clé publique
1. Allez dans **"Account"** → **"General"**
2. Copiez votre **Public Key** (ex: `xxxxxxxxxxxxxxx`)

### Étape 5 : Mettre à jour le code
Dans `index.html`, remplacez :
- `YOUR_PUBLIC_KEY` par votre clé publique
- `YOUR_SERVICE_ID` par votre Service ID  
- `YOUR_TEMPLATE_ID` par votre Template ID

---

## 🎯 Comment ça fonctionne maintenant

1. **Tentative EmailJS** : Envoie l'email directement
2. **Si échec** : Essaie Netlify Forms
3. **Si échec** : Génère un email manuel avec copie automatique

## ✅ Avantages

- ❌ **Plus d'erreur CSRF**
- ✅ **3 méthodes de fallback**
- ✅ **Interface utilisateur identique**
- ✅ **Gratuit et fiable**
- ✅ **Fonctionne partout**

---

## 🚀 Test

1. Remplissez le formulaire
2. Cliquez "Submit My Game"
3. L'email sera envoyé automatiquement !

**Votre email de destination :** `billakpacheme84@gmail.com`
