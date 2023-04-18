---
title: Attribution des aides facultatives à la scolarité
tagline: Simplifiez l'attribution des aides facultatives pour l'équipement des élèves et des étudiants.
tags: cas usage, api particulier, ecole, collège, lycée, université, bourse, boursier, subvention
image: scolarite.jpg
noindex: false # this page will appear on Google
publish: true # this page will appear on /guides page
related_guides:
api:
  - API Particulier
  - API Statut Etudiant
  - API Statut étudiant boursier
  - API Impôt particulier
---

<details>
   <summary>Qu'est-ce que les aides facultatives à la scolarité ?</summary>

Les communes, départements et régions ont mis en place des aides sociales pour aider les familles à financer la scolarité des enfants ou des étudiants.

Ces aides facultatives prennent différentes formes : aide financière, fourniture de matériel informatique, bon d’achat pour des livres. Elle sont conditionnées à certains critères sociaux.

Pour les obtenir, les familles doivent fournir des justificatifs de revenus et/ou de statut.
</details>

## Table des matières

- [Simplifier l'attribution des aides facultatives à la scolarité grâce aux API](#simplifier-l-attribution-des-aides-facultatives-a-la-scolarite-grace-aux-API)
- [Les API et données utiles](#les-api-et-donnees-utiles)
- [Améliorer la délivrance des aides facultatives avec l'API Particulier](#ameliorer-la-delivrance-des-aides-facultatives-avec-l-api-particulier)
  - [Exemple d'application](#exemple-d-application)
- [Demander un accès aux API](#demander-un-acces-aux-api)

## Simplifier l'attribution des aides facultatives à la scolarité grâce aux API 

Collectivités, en intégrant des API dans vos systèmes d'information :

- 😃 les **familles n'ont plus à fournir les justificatifs de leur statut ou de leur revenu (certificat de scolarité, statut boursier, attestation CAF, revenu fiscal de référence, etc.)** pour renseigner leurs demandes d'aides facultatives ;  

- ⏰ Vous accélérez le traitement des dossiers car vos agents n’ont **pas à vérifier les données saisies et les pièces justificatives fournies**, les informations obtenues par les API sous-mentionnées sont certifiées 🔎 ;

- 🎯 Enfin, vous **participez activement à la simplification des démarches pour les citoyens** en mettant en oeuvre le « Dites-le-nous une fois », en application de l’[article L114-8 du Code des relations entre le public et l’administration](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000045213315).


## Les API et données utiles

| API utiles | Données disponibles |  Peut s'utiliser avec FranceConnect |
| --- | --- | --- |
| [API Impôt particulier](/les-api/impot-particulier) - DGFIP | Revenu fiscal de référence, nombre de parts fiscales | ✅ |
| Bouquet [API Particulier](https://particulier.api.gouv.fr/catalogue) - opéré par la DINUM | Quotient familial CAF, composition familiale, statut élève scolarisé et boursier, statut étudiant et étudiant boursier, | ⚙️ Certaines API sont disponibles avec FranceConnect |


## Améliorer la délivrance des aides facultatives avec l'API Particulier

L'API Particulier est un bouquet d'API délivrant des informations administratives des particuliers issues de différents fournisseurs de données.

Avec l'API Particulier, vous avez notamment accès au quotient familial CAF, au statut élève scolarisé et boursier, au statut étudiant et étudiant boursier, au statut demandeur d'emploi...

<Button href="https://particulier.api.gouv.fr/catalogue">Découvrir l'API Particulier</Button>

### Exemple d'application

**Un parent souhaite bénéficier de la fourniture d'un ordinateur pour son enfant scolarisé, depuis le portail de sa commune connecté à l'API Particulier.**

Le parent se connecte à son espace personnel, il clique sur la démarche de demande d'un ordinateur pour les études de son enfant, il **renseigne le nom, prénom, sexe, date de naissance et établissement scolaire de son enfant**.

> ⚙️ **En arrière plan** : Un appel à l'API élève scolarisé du bouquet API Particulier est effectué et permet de vérifier que l'élève est bien scolarisé.

Le parent n'a pas besoin de fournir le certificat de scolarité, la vérification a été faite automatiquement. L'attribution d'un ordinateur étant conditionnée selon les revenus, le parent **renseigne son numéro d'allocataire CAF, son code postal**.

> ⚙️ **En arrière plan** : Un appel à l'API quotient familial CAF du bouquet API Particulier est effectué et permet de récupérer le quotient familial du mois en cours.

La famille est identifiée comme éligible à l'aide. Le parent n'a plus qu'à confirmer sa demande. Du côté de la commune, les agents n'auront pas à vérifier les informations renseignées car celles-ci sont certifiées.


## Demander un accès aux API

### Justifier votre cadre juridique

L'utilisation des données est encadrée légalement. Vous devez formuler une demande auprès de l'API Particulier et/ou des autres API en justifiant du cadre légal de l'utilisation des données :

- Cadre légal général : l'[Article L114-8 du Code des relations entre le public et l'administration](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000045213315) fixe le cadre général qui oblige l’administration à échanger des données lors d’une démarche d’un usager ;

- Cadre légal spécifique aux téléservices : En tant que collectivités territoriales vous avez donc un droit d'accès à certaines données dans le cadre de demandes, services pro-actifs et déclarations usagers. 
L'[Arrêté du 04/07/13 sur les téléservices](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000027697207/#:~:text=Dans%20les%20r%C3%A9sum%C3%A9s-,Arr%C3%AAt%C3%A9%20du%204%20juillet%202013%20autorisant%20la%20mise%20en%20%C5%93uvre,publiques%20locales%20dont%20ils%20sont) détaille à l'article 1 la liste des démarches par secteur. Aidez-vous de cet arrêté pour justifier de votre cadre légal.

- Justificatif des données nécessaires au calcul de la tarification : Il est indispensable de **fournir l'acte/ la délibération** qui fixe les conditions tarifaires et qui permettra d'apprécier finement le droit d'accès à chaque donnée.

### Formulaires de demande d'accès

Les [API disponibles dans l'API Particulier](https://particulier.api.gouv.fr/catalogue) vous intéressent ? Vous n'avez qu'une seule demande d'habilitation à effectuer : 

<Button href="https://datapass.api.gouv.fr/api-particulier">Remplir une demande API Particulier</Button>

Vous avez besoin des données de revenu de la DGFIP ? Il vous faudra faire une [demande d'habilitation dédiée](/les-api/impot-particulier).

⚠️ Lors de votre demande d’habilitation, vous vous engagez à ne demander que les données strictement nécessaires à la réalisation de la démarche administrative.
