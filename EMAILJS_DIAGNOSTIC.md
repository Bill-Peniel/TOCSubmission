# 🔧 Diagnostic EmailJS - Guide de Vérification

## 📋 Vérifications à faire dans votre compte EmailJS

### 1. **Vérifier le Service Email**
1. Connectez-vous à [emailjs.com](https://www.emailjs.com/)
2. Allez dans **"Email Services"**
3. Vérifiez que le service `service_ovyux6e` existe et est **actif**
4. Si le service n'existe pas, créez-en un nouveau

### 2. **Vérifier le Template**
1. Allez dans **"Email Templates"**
2. Vérifiez que le template `template_erc7kby` existe
3. Si le template n'existe pas, créez-en un nouveau avec ce contenu :

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

Fichiers: {{fileCount}} fichiers
- {{fileNames}}

Cordialement,
Tower of Challenge
```

### 3. **Vérifier la Clé Publique**
1. Allez dans **"Account"** → **"General"**
2. Vérifiez que votre **Public Key** est bien `_GmicEt3w9ELpz4_i`
3. Si différent, mettez à jour le code

### 4. **Vérifier les Permissions**
1. Dans **"Email Services"**, assurez-vous que le service est **"Public"**
2. Dans **"Email Templates"**, assurez-vous que le template est **"Public"**

---

## 🚨 Erreurs Communes et Solutions

### **Erreur 400 - Bad Request**
- **Cause** : Template ou Service ID incorrect
- **Solution** : Vérifiez les IDs dans votre dashboard EmailJS

### **Erreur 401 - Unauthorized**
- **Cause** : Clé publique incorrecte ou service privé
- **Solution** : Vérifiez la clé publique et rendez le service public

### **Erreur 403 - Forbidden**
- **Cause** : Template privé ou quota dépassé
- **Solution** : Rendez le template public ou vérifiez votre quota

### **Erreur 500 - Server Error**
- **Cause** : Problème côté EmailJS
- **Solution** : Réessayez plus tard ou contactez le support

---

## 🧪 Test Rapide

1. **Ouvrez la console** (F12)
2. **Soumettez le formulaire**
3. **Regardez les logs** :
   - `📧 Attempting EmailJS send with data:`
   - `🔑 Using Service ID: service_ovyux6e`
   - `📝 Using Template ID: template_erc7kby`
   - `❌ EmailJS failed with error:` (si échec)

4. **Notez l'erreur exacte** et vérifiez selon le guide ci-dessus

---

## 🔄 Configuration Alternative

Si les IDs actuels ne fonctionnent pas, créez une nouvelle configuration :

1. **Nouveau Service** : Créez un service email
2. **Nouveau Template** : Créez un template
3. **Mettez à jour le code** avec les nouveaux IDs

**Votre email de destination :** `billakpacheme84@gmail.com`
