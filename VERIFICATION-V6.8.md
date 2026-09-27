# VELOCE ERP MADA V6.9 — Vérification

## Base
- Base de travail : V6.7.5.
- Stockage local IndexedDB conservé : `veloce_erp_mada_v6_1` afin de ne pas isoler les données existantes.
- Migration d’état : `normalizeState()` initialise `accounting.manualEntries` et conserve les structures V6.x.

## Comptabilité par business
- Module `Comptabilité` disponible dans chaque business.
- BTP et Tilapia conservent leur écran métier dédié et disposent d’un bouton Comptabilité.
- Journal automatique alimenté par achats, ventes, règlements clients, règlements fournisseurs, paie, trésorerie et opérations Tilapia.
- Grand livre.
- Balance générale.
- Bilan synthétique.
- Compte de résultat.
- Tableau des flux de trésorerie.
- Tableau des variations des capitaux propres.
- Annexe synthétique.
- Plan de comptes PCG 2005 intégré.
- Écritures manuelles équilibrées débit/crédit.
- Impression du journal et de la balance.

## Référentiel
Le module est basé sur le PCG 2005 publié par le Ministère des Finances et le Conseil Supérieur de la Comptabilité de Madagascar. Les états générés sont des états ERP de gestion/pré-clôture et doivent être contrôlés par le responsable comptable avant toute déclaration ou dépôt officiel.

## Design
- Hero comptabilité moderne.
- KPIs et onglets tactiles.
- Responsive mobile/tablette.
- Bouton Comptabilité ajouté à la barre d’actions.
- BTP et Tilapia conservent leurs interfaces dédiées.

## Contrôles techniques
- JavaScript extrait de `index.html` validé avec Node.js `--check`.
- Service Worker incrémenté en `veloce-v690`.
- ZIP contrôlé avec `unzip -t`.
