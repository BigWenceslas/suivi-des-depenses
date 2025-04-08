# 🎓 TP – Gestion des Demandes de Remboursement

## 🗂 Modèle de Données (Dataverse)

Ce projet repose sur deux tables principales dans Microsoft Dataverse :

- **Catégories** : contient les types de dépenses (Parking, Restaurant, Autres…)
- **Dépenses** : permet la soumission des demandes de remboursement avec les champs suivants :
  - Nom
  - Description
  - Montant
  - Fichier Justificatif
  - Catégorie (relation N:1 avec la table Catégories)

---

## 🛠 Model-Driven App – Soumission des Demandes

Une application **Model-Driven** a été mise en place pour :
- Créer, lire, modifier et supprimer des enregistrements (CRUD)
- Personnaliser les formulaires et vues
- Intégrer un **Cloud Flow (Power Automate)** :
  - À la soumission d’une dépense, un email de notification est envoyé automatiquement à mon adresse Gmail via un connecteur Gmail lié à mon compte

---

## 🎨 Canvas App – Espace Validateur

Une application **Canvas** dédiée aux validateurs de demandes :

- Au chargement :
  - Affichage des demandes **non révisées** (`Statut = En attente` et `Remboursé = false`)
- Clic sur une **catégorie** :
  - Filtrage des demandes dans une **Gallery**
- Clic sur **Valider** :
  - Ouverture d’un **pop-up de confirmation**
  - Bouton **Non** : met à jour le statut à `Rejeté`
  - Bouton **Oui** : met à jour le statut à `Accepté` et le champ `Remboursé` à `true`

---

## ⚠️ Difficultés Rencontrées

- Quelques difficultés à configurer un **dashboard** pour l’affichage global des données
- **Instabilité de la connexion réseau**, provoquant des erreurs et empêchant l’autocomplétion dans Power Apps Studio

---

## 📌 Prochaine Étape

En attente d’un **meeting de revue**, des améliorations continues sont en cours (UX, validation, performances).

