# Ma Liste d'Épicerie — Démo

Petit site statique bilingue (FR/EN) pour tester l'app **sans compte** (mode démo) et avec **page Dons** qui s'ouvre automatiquement.

## Fonctionnalités
- 🇫🇷/🇬🇧 **Bilingue** avec bascule FR/EN (détection automatique, mémorisation).
- 🧪 **Mode Démo (invité)**: données en `sessionStorage`, effacées à la fermeture de l’onglet ou après 30 min d’inactivité (bouton **Reset** inclus).
- 🧾 **Liste d'épicerie**: ajout d’articles (emoji, quantité, unité, prix, note, mini-photo). Suppression des éléments cochés. Envoi vers **Garde‑manger**.
- 🥫 **Garde‑manger**: ajout manuel, compteur “Depuis…”, bouton **Utiliser** pour décrémenter.
- 🍳 **Recettes** et 📅 **Planning**: exemples simples (démo visuelle).
- 💛 **Dons**: boutons à montants fixes et montant personnalisé, liens vers PayPal.me.
- 💡 **Page Dons qui s’ouvre automatiquement** à chaque lancement (modal).
- 🎨 **Design** moderne sombre (cartes, coins arrondis, ombres, dégradés).

## Déploiement
1. **Téléchargez le ZIP**.
2. Uploadez le dossier sur **GitHub** (nouveau repo).
3. Activez **GitHub Pages** (branche `main` / dossier `/root`).
4. Ouvrez l’URL de Pages (ça marche 100% statique).

## Personnalisation
- **Nom PayPal** : modifiez `PAYPAL_BASE` dans `index.html` (rechercher `paypal.me/malistedepicerie`).
- **Langue par défaut** : déduite du navigateur, sinon forcer en modifiant `detectDefaultLang()`.
- **Auto‑ouverture Dons** : la modale s’ouvre sur chaque lancement dans `DOMContentLoaded` → `openDonationsModal()`.

## Limitations
- Pas de backend: en mode **auth**, les données persistent seulement dans `localStorage` (à remplacer par votre API plus tard).
- En **mode démo**, aucune donnée n’est envoyée côté serveur et tout est supprimé à la fin de session.

— Build 2025-08-30
