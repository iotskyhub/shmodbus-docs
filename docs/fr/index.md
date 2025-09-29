# SHModbus - Guide Utilisateur

![Application SHModbus](../shared-images/shmodbus-app.png)

## Aperçu

SHModbus Client est une application de surveillance et de visualisation de données industrielles en temps réel qui se connecte aux appareils Modbus et affiche les données de capteurs en direct, l'état des équipements et les informations système via une interface web intuitive.

## Fonctionnalités Clés

### Surveillance de Données en Temps Réel
- **Tableau de Données en Direct**: Visualisez les valeurs en temps réel des appareils Modbus connectés avec des mises à jour automatiques
- **Auto-actualisation**: Les données se mettent à jour automatiquement toutes les quelques secondes sans actualisation manuelle
- **Affichage d'Horodatage**: Voyez exactement quand chaque point de données a été mis à jour pour la dernière fois
- **Formatage des Valeurs**: Toutes les valeurs numériques s'affichent avec une précision cohérente de 2 décimales

### Visualisation de Données
- **Graphiques Interactifs**: Représentation visuelle des tendances de données dans le temps
- **Types de Graphiques Multiples**: Graphiques linéaires, en barres et autres options de visualisation
- **Données Historiques**: Visualisez les tendances et modèles de données passées
- **Zoom et Panoramique**: Interagissez avec les graphiques pour vous concentrer sur des périodes spécifiques

### Gestion des Appareils
- **Statut de Connexion**: Indication en temps réel de la connectivité des appareils Modbus
- **Informations sur les Appareils**: Visualisez les détails sur les équipements et capteurs connectés
- **Support Multi-Appareils**: Surveillez plusieurs appareils Modbus simultanément
- **Santé de Connexion**: Les indicateurs visuels montrent quand les appareils sont en ligne/hors ligne

### Fonctionnalités de l'Interface Utilisateur
- **Design Réactif**: Fonctionne sur les ordinateurs de bureau, tablettes et appareils mobiles
- **Thème Sombre/Clair**: Choisissez votre thème visuel préféré
- **Tableaux Triables**: Cliquez sur les en-têtes de colonnes pour trier les données par n'importe quel champ
- **Recherche et Filtrage**: Trouvez rapidement des points de données spécifiques
- **Capacités d'Export**: Sauvegardez les données dans des fichiers pour analyse externe

### Communication en Temps Réel
- **Intégration SignalR**: Mises à jour instantanées des données sans actualisation de page
- **Notifications en Direct**: Alertes immédiates lorsque l'état de l'appareil change
- **Reconnexion Automatique**: Maintient la connexion même pendant les interruptions réseau
- **Faible Latence**: Délai minimal entre les mises à jour d'appareil et l'affichage

### Gestion des Données
- **Données en Cache**: Valeurs récentes stockées localement pour un accès rapide
- **Historique des Données**: Accès aux lectures historiques et tendances
- **Validation des Valeurs**: Détection automatique et traitement des données invalides
- **Support des Fuseaux Horaires**: Affiche les heures dans votre fuseau horaire local

## Applications Industrielles

- **Surveillance de Processus**: Suivez la température, pression, débits et autres variables de processus
- **Statut d'Équipement**: Surveillez les vitesses de moteur, positions de vannes, statut de pompes
- **Surveillance d'Alarmes**: Alertes en temps réel pour les conditions hors limites
- **Contrôle Qualité**: Suivez les métriques de production et paramètres de qualité
- **Gestion Énergétique**: Surveillez la consommation d'énergie et les métriques d'efficacité

## Fonctionnalités d'Accessibilité

- **Navigation au Clavier**: Contrôle complet de l'application en utilisant seulement le clavier
- **Support de Lecteur d'Écran**: Compatible avec les technologies d'assistance
- **Options de Contraste Élevé**: Visibilité améliorée pour les utilisateurs avec déficiences visuelles
- **Interface Évolutive**: Tailles de texte et d'éléments ajustables

## Optimisation des Performances

- **Mises à Jour Efficaces**: Actualise seulement les données qui ont réellement changé
- **Optimisation de Bande Passante**: Usage réseau minimal pour surveillance continue
- **Compatibilité Navigateur**: Fonctionne avec tous les navigateurs web modernes
- **Chargement Rapide**: Démarrage rapide et interface réactive

## Options de Configuration

- **Vues Personnalisables**: Arrangez les affichages de données selon votre flux de travail
- **Préférences Utilisateur**: Sauvegardez vos paramètres et dispositions préférés
- **Sélection de Points de Données**: Choisissez quels capteurs et valeurs surveiller
- **Intervalles de Mise à Jour**: Ajustez la fréquence d'actualisation des données

## Fonctionnalités de Sécurité

- **Connexions Sécurisées**: Communication chiffrée avec appareils et serveurs
- **Authentification Utilisateur**: Contrôle d'accès et gestion des utilisateurs
- **Intégrité des Données**: Vérification que les données affichées sont précises et inchangées
- **Piste d'Audit**: Journalisation des actions utilisateur et événements système

## Cas d'Usage Courants

- **Fabrication**: Surveillez l'équipement de ligne de production et métriques de qualité
- **Systèmes CVC**: Suivez température, humidité et qualité de l'air
- **Traitement de l'Eau**: Surveillez débits, niveaux chimiques et statut de pompes
- **Systèmes Énergétiques**: Suivez génération, consommation et efficacité énergétiques
- **Automatisation de Bâtiment**: Surveillez éclairage, sécurité et systèmes environnementaux
- **Équipement de Laboratoire**: Suivez conditions de test et résultats de mesures

## Premiers Pas

1. Ouvrez l'application dans votre navigateur web
2. Attendez l'établissement de la connexion avec les appareils Modbus
3. Visualisez les données en temps réel dans le Tableau en Direct
4. Explorez graphiques et visualisations pour les tendances
5. Personnalisez votre vue en triant et filtrant les données
6. Configurez alertes et surveillance pour paramètres critiques

L'application gère automatiquement tous les détails techniques de la communication Modbus, formatage des données et mises à jour en temps réel, vous permettant de vous concentrer sur la surveillance de vos processus industriels et équipements.