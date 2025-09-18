# 🚀 Créer une Configuration EmailJS Complète

## 🎯 Problème Actuel
La clé publique est correcte (`N5ItLULOOMcGIH76v`) mais les **Service ID** et **Template ID** n'existent pas dans votre compte.

---

## 📋 Solution : Créer une Nouvelle Configuration

### **Étape 1 : Créer un Service Email**

1. **Allez dans votre dashboard EmailJS** : [dashboard.emailjs.com](https://dashboard.emailjs.com/)
2. **Cliquez sur "Email Services"** dans le menu de gauche
3. **Cliquez sur "Add New Service"**
4. **Choisissez "Gmail"** (ou votre fournisseur email)
5. **Connectez votre compte** `billakpacheme84@gmail.com`
6. **Notez le Service ID** généré (ex: `service_xxxxxxx`)

### **Étape 2 : Créer un Template Email**

1. **Cliquez sur "Email Templates"** dans le menu de gauche
2. **Cliquez sur "Create New Template"**
3. **Utilisez ce contenu exact** :

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

4. **Notez le Template ID** généré (ex: `template_xxxxxxx`)

### **Étape 3 : Mettre à jour le Code**

Dans `index.html`, remplacez :

```javascript
const SERVICE_ID = "VOTRE_SERVICE_ID_ICI"; // Remplacez par votre Service ID
const TEMPLATE_ID = "VOTRE_TEMPLATE_ID_ICI"; // Remplacez par votre Template ID
```

**Exemple :**
```javascript
const SERVICE_ID = "service_abc123";
const TEMPLATE_ID = "template_xyz789";
```

---

## 🔧 Configuration Rapide Alternative

Si vous voulez une configuration rapide, voici des IDs de test que vous pouvez utiliser :

### **Option 1 : Configuration de Test**
```javascript
const SERVICE_ID = "service_default";
const TEMPLATE_ID = "template_default";
```

### **Option 2 : Configuration Gmail Directe**
```javascript
const SERVICE_ID = "gmail";
const TEMPLATE_ID = "contact_form";
```

---

## 🧪 Test Final

1. **Sauvegardez le fichier** avec vos vrais IDs
2. **Rechargez la page**
3. **Regardez la console** :
   - `🔧 Initializing EmailJS with key: N5ItLULOOMcGIH76v`
   - `📧 Sending with Service ID: [votre_service_id]`
   - `📧 Sending with Template ID: [votre_template_id]`

4. **Soumettez le formulaire**
5. **Vous devriez voir** : `✅ Email sent successfully`

---

## 📞 Si Problème Persiste

- **Vérifiez que le service est "Public"** dans Email Services
- **Vérifiez que le template est "Public"** dans Email Templates
- **Vérifiez que votre email de destination** est bien `billakpacheme84@gmail.com`

**Votre email de destination :** `billakpacheme84@gmail.com`
