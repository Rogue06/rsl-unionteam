# Guide Git - UNION TEAM Dashboard

Ce guide explique comment enregistrer et pousser tes modifications sur le repository GitHub.

**Repository :** https://github.com/Rogue06/rsl-unionteam.git

---

## Résumé des travaux effectués (à commiter)

- **Version compressée** : Bouton "Copier version compressée" dans le menu (≤2000 caractères pour Discord)
- **Vue compressée** : Onglet de prévisualisation avec sync scroll + surlignage jaune
- **Règles de compression** : Intro raccourcie, suppression des mots non essentiels, format `place(s)=X`
- **Centre d'aide** : Documentation mise à jour (version 4.1)

---

## Étape 1 : Vérifier l'état du projet

Ouvre un terminal dans le dossier du projet et exécute :

```bash
cd /Users/rogue/Desktop/rsl-unionteam
git status
```

Tu verras les fichiers modifiés (ex. `index.html`).

---

## Étape 2 : Ajouter les fichiers (git add)

Pour ajouter **tous** les fichiers modifiés :

```bash
git add .
```

Pour ajouter **un seul fichier** :

```bash
git add index.html
```

---

## Étape 3 : Commiter (git commit)

Un commit enregistre tes modifications avec un message descriptif.

```bash
git commit -m "Add compressed version feature for Discord 2000 char limit"
```

**Exemples de messages courts et clairs :**

| Message | Signification |
|---------|---------------|
| `Add compressed version feature for Discord 2000 char limit` | Ajout de la version compressée |
| `Add version compressée with preview and sync scroll` | Version compressée + preview + scroll |
| `Fix: add yellow highlight in compressed view` | Correction du surlignage jaune |

**Message recommandé pour ce commit :**

```bash
git commit -m "Add compressed version feature (≤2000 chars) with preview, sync scroll and highlight"
```

---

## Étape 4 : Pousser (git push)

Envoie tes commits sur GitHub :

```bash
git push origin main
```

Si c'est la première fois, configure le remote :

```bash
git remote add origin https://github.com/Rogue06/rsl-unionteam.git
git push -u origin main
```

---

## Commande tout-en-un

Pour faire tout d'un coup (add + commit + push) :

```bash
git add . && git commit -m "Add compressed version feature (≤2000 chars) with preview, sync scroll and highlight" && git push origin main
```

---

## En cas de problème

**Si le push est refusé :**
```bash
git pull origin main
git push origin main
```

**Si tu veux annuler le dernier commit (avant push) :**
```bash
git reset --soft HEAD~1
```

**Voir l'historique des commits :**
```bash
git log --oneline
```

---

## Bonnes pratiques

1. **Commit souvent** : Un commit par fonctionnalité ou correction
2. **Messages en anglais** : Courts, clairs, descriptifs
3. **Vérifier avant push** : `git status` et `git diff` pour voir les changements
