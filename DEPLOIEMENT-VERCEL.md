# 🚀 Déploiement sur Vercel - Hôtel Les Tourrades

## 📋 Prérequis
- Un compte GitHub (gratuit)
- Un compte Vercel (gratuit)
- Votre nom de domaine **hotel-lestourrades.fr**

---

## ⚡ MÉTHODE RAPIDE (Recommandée)

### Étape 1 : Créer un compte Vercel
1. Allez sur https://vercel.com
2. Cliquez sur **"Sign Up"**
3. Inscrivez-vous avec GitHub (recommandé) ou email

### Étape 2 : Déployer le site
1. Une fois connecté, cliquez sur **"Add New Project"**
2. Sélectionnez **"Import Third-Party Git Repository"** ou **"Continue with GitHub"**

**OU utilisez la méthode drag & drop :**

1. Sur le tableau de bord Vercel, cliquez sur **"Add New"** → **"Project"**
2. Cliquez sur **"Deploy from a template"** ou cherchez l'option de déploiement direct
3. OU : téléchargez Vercel CLI (voir Méthode 2 ci-dessous)

---

## 🎯 MÉTHODE 1 : Via GitHub (Recommandée pour les mises à jour futures)

### 1. Créer un repository GitHub

1. Allez sur https://github.com
2. Cliquez sur **"New repository"**
3. Nom : `hotel-lestourrades`
4. Cochez **"Add a README file"**
5. Cliquez sur **"Create repository"**

### 2. Uploader les fichiers

1. Dans votre repository, cliquez sur **"Add file"** → **"Upload files"**
2. Glissez-déposez tous les fichiers :
   - index.html
   - vercel.json
   - Le dossier **images/** complet (avec toutes les photos)
3. Cliquez sur **"Commit changes"**

### 3. Déployer sur Vercel

1. Retournez sur https://vercel.com
2. Cliquez sur **"Add New Project"**
3. Sélectionnez **"Import Git Repository"**
4. Choisissez votre repository `hotel-lestourrades`
5. Cliquez sur **"Deploy"**
6. ✅ Votre site sera en ligne en quelques secondes !

Vous obtiendrez une URL temporaire : `hotel-lestourrades.vercel.app`

---

## 🎯 MÉTHODE 2 : Via Vercel CLI (Ligne de commande)

### 1. Installer Vercel CLI

```bash
npm install -g vercel
```

### 2. Se connecter

```bash
vercel login
```

### 3. Déployer

1. Ouvrez un terminal
2. Naviguez vers le dossier contenant vos fichiers :
   ```bash
   cd chemin/vers/votre/dossier
   ```
3. Lancez le déploiement :
   ```bash
   vercel
   ```
4. Répondez aux questions :
   - Set up and deploy? **Y**
   - Which scope? Choisissez votre compte
   - Link to existing project? **N**
   - Project name? `hotel-lestourrades`
   - In which directory? **./  (dossier actuel)**
   - Want to override settings? **N**

---

## 🌐 CONFIGURER VOTRE DOMAINE PERSONNALISÉ

### Étape 1 : Ajouter le domaine sur Vercel

1. Dans votre projet Vercel, allez dans **"Settings"**
2. Cliquez sur **"Domains"**
3. Entrez : `hotel-lestourrades.fr`
4. Cliquez sur **"Add"**
5. Vercel vous donnera des enregistrements DNS à configurer

### Étape 2 : Configurer le DNS

Vous allez recevoir quelque chose comme :

**Type A Record:**
```
Type: A
Name: @
Value: 76.76.21.21
```

**Type CNAME (pour www):**
```
Type: CNAME
Name: www
Value: cname.vercel-dns.com
```

### Étape 3 : Chez votre registrar (OVH, Gandi, etc.)

1. Connectez-vous à votre compte où vous avez acheté **hotel-lestourrades.fr**
2. Allez dans la gestion DNS du domaine
3. Ajoutez les enregistrements fournis par Vercel :
   - **Enregistrement A** : Pointez `@` vers l'IP de Vercel
   - **Enregistrement CNAME** : Pointez `www` vers `cname.vercel-dns.com`
4. Supprimez tout ancien enregistrement A ou CNAME conflictuel
5. Sauvegardez

### Étape 4 : Vérification

1. Retournez sur Vercel
2. Dans **Domains**, cliquez sur **"Verify"**
3. ✅ Une fois vérifié (peut prendre 24-48h), votre site sera accessible sur **hotel-lestourrades.fr**

---

## 📂 Structure des fichiers à uploader

Voici ce que votre projet doit contenir :

```
hotel-lestourrades/
├── index.html
├── vercel.json
└── images/
    ├── facade.jpg
    ├── reception.jpg
    ├── chambre1.jpg
    ├── chambre2.jpg
    ├── chambre3.jpg
    ├── chambre4.jpg
    └── salle-bain.jpg
```

---

## ⚙️ Configuration DNS détaillée

### Si votre domaine est chez OVH :

1. Connexion à l'espace client OVH
2. Aller dans **"Web Cloud"** → **"Noms de domaine"**
3. Cliquer sur **hotel-lestourrades.fr**
4. Onglet **"Zone DNS"**
5. Cliquer sur **"Ajouter une entrée"**
6. Ajouter :
   - **Type A** : `@` → IP de Vercel
   - **Type CNAME** : `www` → `cname.vercel-dns.com`

### Si votre domaine est chez Gandi :

1. Aller sur https://admin.gandi.net
2. **"Mes domaines"** → **hotel-lestourrades.fr**
3. **"Enregistrements DNS"**
4. Ajouter les enregistrements Vercel

### Si votre domaine est chez Cloudflare :

1. Dans le tableau de bord Cloudflare
2. Sélectionnez **hotel-lestourrades.fr**
3. **DNS** → **Records**
4. Ajouter les enregistrements Vercel
5. ⚠️ Désactivez le proxy orange (cliquez dessus pour passer en gris)

---

## 🎉 Avantages de Vercel

✅ **Gratuit** pour les sites statiques
✅ **HTTPS automatique** (SSL gratuit)
✅ **CDN mondial** (site ultra-rapide partout)
✅ **Déploiement automatique** quand vous modifiez sur GitHub
✅ **Zéro configuration** nécessaire
✅ **Analytics inclus** (statistiques de visite)
✅ **Formulaire de contact** fonctionne via mailto

---

## 🔄 Mises à jour futures

### Via GitHub :
1. Modifiez vos fichiers sur GitHub
2. Le site se met à jour automatiquement !

### Via CLI :
1. Modifiez vos fichiers localement
2. Tapez `vercel --prod`
3. Le site est mis à jour !

---

## 📧 Email de réservation

Le formulaire continue d'envoyer les réservations à :
**hotellestourrades@orange.fr**

Aucune configuration supplémentaire nécessaire !

---

## 🆘 Problèmes courants

### Le domaine ne fonctionne pas après 48h
- Vérifiez que les enregistrements DNS sont corrects
- Utilisez https://dnschecker.org pour vérifier la propagation

### Les images ne s'affichent pas
- Vérifiez que le dossier `images/` est bien uploadé
- Vérifiez les majuscules/minuscules dans les noms de fichiers

### Erreur 404
- Vérifiez que `index.html` est à la racine du projet
- Vérifiez que `vercel.json` est présent

---

## 📞 Support

- Documentation Vercel : https://vercel.com/docs
- Support Vercel : https://vercel.com/support
- Communauté : https://github.com/vercel/vercel/discussions

---

## ✨ Résumé rapide

1. Créer compte Vercel (gratuit)
2. Créer repository GitHub
3. Uploader les fichiers (index.html + images + vercel.json)
4. Connecter le repo à Vercel
5. Ajouter le domaine dans Vercel
6. Configurer le DNS chez votre registrar
7. ✅ C'est en ligne !

**Temps estimé : 15-30 minutes**
**Coût : Gratuit sur Vercel + coût du nom de domaine**
