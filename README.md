# monmatchcarbone 🌍🥵

Ici résident les modèles de calcul et les données de https://monmatchcarbone.fr.

### Ecriture des modèles du simulateur

Le modèle d'empreinte climat personnelle est écrit dans un français le plus lisible possible : 

```yaml
# Premier extrait 
transport . deux roues thermique: 
  icônes: 🛵
  applicable si: présent
  formule: empreinte * km * nombre de mois

transport . deux roues thermique . présent:
  question: Scooter ou moto ?
  description: |
    Les scooters et motos sont aujourd'hui très majoritairement des engins qui fonctionnent au pétrole. Les équivalents électriques ont fait leur apparition, mais timidement.
  par défaut: non

transport . deux roues thermique . km: 
  question: Combien de km faites-vous par mois avec votre scooter ou moto pour vous rendre à une activité sportive ? 
  par défaut: 100 km/mois
  unité: km/mois


### code de l'interface

Le code du simulateur ici [`pascalbes/monmatchcarbone-site`](https://github.com/pascalbes/monmatchcarbone-site).

Il repose sur le nouveau langage de programmation `publicodes` documenté sur https://publi.codes.
