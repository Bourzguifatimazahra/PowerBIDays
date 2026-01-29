# 📊 Power BI – Analyse des Performances Commerciales 2020

![Logo Pro](https://img.shields.io/badge/Power_BI-Professional-blue?style=for-the-badge&logo=powerbi&logoColor=yellow)  
![Version](https://img.shields.io/badge/Version-1.0.0-green)  
![Date](https://img.shields.io/badge/Soumission-28_Janvier_2026-orange)  
![License](https://img.shields.io/badge/License-Academic_Use-lightgrey)

## 🎯 **Objectif du Projet**
Créer un tableau de bord interactif sous **Microsoft Power BI** pour analyser les performances commerciales de l'année **2020** à partir d'une base de données relationnelle **AdventureWorks (version étendue)**. Ce projet transforme des données brutes en insights actionnables pour les décideurs métier.

## 🛠 **Modèle de Données (Star Schema)**

### **Tables Utilisées (9)**
| Table | Type | Description |
|-------|------|-------------|
| **Sales** | Fait | Transactions commerciales |
| **Products** | Dimension | Informations produits |
| **Customers** | Dimension | Informations clients |
| **Calendar** | Dimension | Dates et périodes |
| **Territory** | Dimension | Zones géographiques |
| **Budget** | Fait | Données budgétaires |
| **BudgetPeriod** | Dimension | Périodes budgétaires |
| **DimProductCategory** | Dimension | Catégories produits |
| **DimProductSubcategory** | Dimension | Sous-catégories produits |

### **Relations (9)**
- `Sales[ProductKey]` → `Products[ProductKey]`
- `Sales[CustomerKey]` → `Customers[CustomerKey]`
- `Sales[DateKey]` → `Calendar[DateKey]`
- `Sales[TerritoryKey]` → `Territory[TerritoryKey]`
- `Budget[PeriodKey]` → `BudgetPeriod[PeriodKey]`
- `Products[CategoryKey]` → `DimProductCategory[CategoryKey]`
- `Products[SubcategoryKey]` → `DimProductSubcategory[SubcategoryKey]`
- `Budget[ProductKey]` → `Products[ProductKey]`
- `Budget[TerritoryKey]` → `Territory[TerritoryKey]`

---

## 📈 **Mesures DAX (30 KPIs)**

| Catégorie | Mesure | Description |
|-----------|--------|-------------|
| **Ventes** | Total Sales | Chiffre d'affaires total |
| | Total Orders | Nombre de commandes |
| | Total Customers | Nombre de clients uniques |
| | Total Quantity | Quantité vendue |
| | Sales LY | Ventes année précédente |
| | YoY Growth % | Croissance annuelle en % |
| | Sales per Territory | Ventes par zone |
| **Rentabilité** | Profit Margin % | Marge bénéficiaire |
| | Gross Profit | Profit brut |
| | Gross Margin % | Marge brute en % |
| | Profit per Unit | Profit par unité |
| | Profit per Customer | Profit par client |
| **Commandes** | Average Order Value | Valeur moyenne commande |
| | Units per Order | Unités moyennes/commande |
| | Average Basket Size | Panier moyen en quantité |
| | Orders Count | Nombre de lignes commandes |
| **Budget** | Total Budget | Budget total |
| | Budget Variance | Écart vs budget |
| | Budget Achievement % | Taux réalisation budget |
| | Atteinte Objectif % | Taux atteinte objectifs |
| **Coûts** | Total Cost | Coût total |
| | Total Product Cost | Coût produit total |
| | Unit Cost Average | Coût unitaire moyen |
| | Total Discounts | Remises totales |
| **Clients** | Revenue per Customer | CA par client |
| | Year-over-Year Growth | Croissance en valeur |
| **Formattage** | Ventes Réelles bn | Ventes en milliards |
| | Budget Total bn | Budget en milliards |
| | Ecart Budget | Alias Budget Variance |
| | Sales per Month | Ventes mensuelles |

---

## 📊 **Visuels Personnalisés Implémentés**

| Visuel | Type | Justification |
|--------|------|---------------|
| **🌍 Customer World Flag** | Carte avec drapeaux | Visualisation géographique engageante des clients |
| **🔍 Text Filter** | Filtre texte interactif | Recherche rapide dans les données |
| **🎯 Bullet Chart 2.4.20** | Graphique cible | Suivi d'objectifs vs performance |
| **📊 Infoviver Analytics +** | Tableau enrichi | Affichage multi-KPIs avec formatage conditionnel |
| **▶️ Play Axis** | Contrôle temporel | Animation de l'évolution des données dans le temps |
| **🗺️ Choropleth Map** | Carte géographique | Analyse spatiale avec dégradés de couleur |

---

## 🎨 **Pages du Rapport (5 pages)**

### **1. Vue d'Ensemble**
- **Titre :** *Tableau de Bord Exécutif 2020*
- **Contenu :** KPIs principaux, ventes mensuelles, filtres globaux
- **Story :** Donne une vision consolidée des performances annuelles

### **2. Analyse Produits**
- **Titre :** *Rentabilité par Catégorie*
- **Contenu :** Répartition profit, marge vs volume, analyse par sous-catégorie
- **Story :** Identifie les produits les plus rentables et leur performance temporelle

### **3. Comportement Client**
- **Titre :** *Portrait Client & Fidélité*
- **Contenu :** Top clients, profit par client, distribution géographique
- **Story :** Met en lumière les segments clients les plus valorisants

### **4. Suivi Budgétaire**
- **Titre :** *Performance vs Budget*
- **Contenu :** Écarts budgétaires, atteinte d'objectifs, analyse par segment
- **Story :** Évalue l'efficacité de la planification financière

### **5. Dynamique Temporelle**
- **Titre :** *Évolution & Tendances*
- **Contenu :** Animation des ventes, croissance YoY, comparaisons mensuelles
- **Story :** Analyse les tendances et prépare la planification future

---

## 🚀 **Guide d'Utilisation**

### **Prérequis**
- Microsoft Power BI Desktop (version récente)
- Accès au fichier `.pbix`

### **Étapes**
1. **Télécharger** le fichier `Performance_Commerciale_2020.pbix`
2. **Ouvrir** avec Power BI Desktop
3. **Rafraîchir les données** si nécessaire (Fichier → Options → Sources de données)
4. **Naviguer** entre les pages via l'onglet en bas
5. **Interagir** avec les visuels :
   - Utiliser les slicers (mois, catégorie, pays)
   - Cliquer sur les graphiques pour filtrer croisé
   - Utiliser le Play Axis pour animer l'évolution temporelle
   - Rechercher avec le Text Filter

### **Personnalisation**
- Modifier les mesures DAX via "Modèle de données"
- Ajouter de nouvelles pages avec "Nouvelle page"
- Changer les visuels via le volet "Visualisations"

---

## 📋 **Exigences du Projet Respectées**

| Exigence | Statut |
|----------|--------|
| ✅ Base de données relationnelle multi-tables | ✔️ 9 tables |
| ✅ Modèle en étoile avec clés primaires/étrangères | ✔️ 9 relations |
| ✅ Minimum 10 KPIs définis | ✔️ 30 mesures DAX |
| ✅ Minimum 3 visuels personnalisés | ✔️ 6 visuels implémentés |
| ✅ Tableau de bord interactif | ✔️ 5 pages avec filtres |
| ✅ Présentation claire avec storytelling | ✔️ Documentation complète |
| ✅ Fichier .pbix fonctionnel | ✔️ Inclus dans le dépôt |

---

## 📄 **Présentation du Projet**

### **Points Clés à Présenter :**
1. **Choix du Dataset :** AdventureWorks étendu pour sa richesse et son réalisme
2. **KPIs Identifiés :** 30 mesures couvrant ventes, rentabilité, clients et budget
3. **Modèle de Données :** Schéma en étoile optimisé pour les performances
4. **Visuels Personnalisés :** Chaque visuel justifié par un besoin métier spécifique
5. **Insights Découverts :** 
   - Les vélos représentent 95% du profit brut
   - Écart budgétaire négatif dans 3 segments clés
   - Croissance de 12% YoY malgré le contexte 2020

---

## 👨‍💻 **Auteur**
**Nom :** Bourzgui Fatima Zahra    
 

 

**✨ Merci d'utiliser ce tableau de bord Power BI ! ✨**
