# Serveur

```{note}

J'ai créé un nom de domaine et un hébergement ave LWS.

```

## Arborescence

```{note}

Insérer image

```

Ces dossiers correspondent à la structure classique d’un serveur web ou à une configuration spécifique fournie par LWS (ou un hébergeur similaire). Voici une description des dossiers couramment présents et leur utilité :

### **.well-known**
- **Description** : Ce dossier est utilisé pour des fichiers standardisés qui permettent des échanges spécifiques entre le serveur et des services externes, comme l’autorisation de certificats SSL/TLS (par exemple, Let's Encrypt) ou des validations pour des outils divers.

---

### **bin**
- **Description** : Contient généralement des fichiers exécutables ou des scripts nécessaires au fonctionnement du serveur. Ce dossier peut rester vide si vous n’avez pas installé de logiciels personnalisés.

---

### **cgi-bin**
- **Description** : Répertoire destiné aux scripts CGI (Common Gateway Interface), comme des scripts en Perl ou Python, permettant de traiter des requêtes HTTP dynamiquement.

---

### **dev**
- **Description** : Ce répertoire est rarement modifié directement par un utilisateur. Il est souvent réservé aux fichiers liés aux périphériques ou aux configurations système.

---

### **etc**
- **Description** : Contient les fichiers de configuration du serveur ou d’applications installées. Par exemple, les fichiers de configuration PHP ou Apache pourraient s’y trouver.

---

### **exec_dir**
- **Description** : Dossier personnalisé par LWS où peuvent être placés des fichiers exécutables. Similaire au dossier `bin`, mais avec une logique d'organisation propre à cet hébergeur.

---

### **home**
- **Description** : Ce dossier correspond souvent à votre espace personnel ou utilisateur sur le serveur. Les sous-dossiers pour des utilisateurs spécifiques (ou vos sites) pourraient s’y trouver.

---

### **htdocs**
- **Description** : C’est généralement **le dossier principal où placer vos fichiers web**, comme vos fichiers HTML, CSS, JavaScript, et autres ressources. Par convention, c’est la racine publique du serveur web.

---

### **lib** et **lib64**
- **Description** : Ces répertoires contiennent des bibliothèques nécessaires pour exécuter certaines applications ou services du serveur. La distinction entre `lib` et `lib64` est liée aux architectures 32 bits et 64 bits.

---

### **log**
- **Description** : Ce dossier contient les journaux (logs) du serveur. Ils peuvent inclure :
  - Les erreurs générées par le serveur web (Apache, Nginx, etc.).
  - Les journaux des accès au site.
  - Des fichiers de log spécifiques à vos applications.

---

### **opt**
- **Description** : Utilisé pour des logiciels ou des applications optionnelles installées manuellement ou par l’hébergeur.

---

### **sftproot**
- **Description** : Ce dossier peut être le point de départ de votre connexion SFTP (ou FTP sécurisé). Les fichiers que vous téléchargez via SFTP peuvent être stockés ici temporairement avant d’être déplacés.

---

### **tmp**
- **Description** : Un répertoire temporaire pour les fichiers générés par le serveur ou vos scripts. Pensez à le nettoyer régulièrement.

---

### **usr**
- **Description** : Contient des fichiers utilisateur partagés ou des bibliothèques additionnelles pour le système. C’est un répertoire classique dans des systèmes Linux.

---

### **var**
- **Description** : Utilisé pour les fichiers variables ou dynamiques, comme :
  - Les bases de données locales.
  - Les fichiers temporaires générés par les applications.

---

### Ce qui est essentiel pour vous :
1. **htdocs** : Placez vos fichiers web ici pour qu’ils soient accessibles en ligne.
2. **log** : Consultez ce répertoire en cas de problème pour identifier des erreurs.
3. **tmp** : Utilisez-le pour des fichiers temporaires si nécessaire.

Si vous avez d’autres questions ou besoin d’aide pour une configuration spécifique, n’hésitez pas !