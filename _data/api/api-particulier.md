---
title: API Particulier
tagline: Entités administratives, simplifiez les démarches des particuliers en récupérant pour eux leurs informations administratives (quotient familial CAF, composition familiale, statut demandeur d’emploi, étudiant et étudiant boursier).
is_open: -1 # -1 means API not open
datapass_link: https://datapass.api.gouv.fr/api-particulier
access_page:
  - who:
      - Un particulier ou une entreprise
    is_eligible: -1
    description: |
      Seules les administrations sont habilitées à utiliser API Particulier.

      <Button href="/rechercher-api">Rechercher une autre API</Button>
  - who:
      - Une collectivité ou une administration
    is_eligible: 1
    description: |
      Conformément aux dispositions de <External href="https://www.legifrance.gouv.fr/affichCodeArticle.do?cidTexte=LEGITEXT000031366350&idArticle=LEGIARTI000031367412&dateTexte=&categorieLien=cid">l'article L114-8</External> du *code des relations entre le public et l'administration*, seules les administrations sont habilitées à échanger entre elles des informations ou données strictement nécessaires pour traiter une démarche.

      Pour obtenir un agrément, vous devez **justifier d'une simplification pour les citoyens**, et vous engager à
      n'accéder aux données personnelles qu'avec **l'accord explicite** de l'usager.

      <NextSteps />
      <QuestionTree tree='api-particulier' question='apipart'/>
  - who:
      - Un éditeur de logiciel
    is_eligible: -1
    description: |
      Si vous êtes **éditeur de logiciels, c'est à votre collectivité ou administration de faire sa demande d'habilitation.**

      En revanche, vous pouvez nous demander de vous référencer sur un cas d'usage afin de proposer des formulaires pré-remplis et ainsi simplifier l'expérience de vos clients publics.

      <Button href="https://form.typeform.com/to/GU90FCIE">Demander à être référencé</Button>
stat:
  lastXdays: 30
  url: https://status.api.gouv.fr/
  label: justificatifs papier évités
partners:
  - CNAF
  - pole-emploi
  - mesr
producer: dinum
keywords:
  - Quotient familial
  - statut
  - étudiant
  - demandeur
  - emploi
  - ccas
  - adresse
  - justificatif de domicile
  - bourse
  - boursier
  - famille
  - enfant
  - crous
  - cnous
  - caf
  - études
  - établissement
  - certificat de scolarité
  - échelon
  - particulier
  - citoyen
  - aide
  - tarification
  - démarche
  - guichet
  - scolarité
  - indémnisation
  - chomage
rate_limiting_resume: 20 appels / seconde / jeton
rate_limiting_description: |
  L'API est disponible à hauteur de 20 appels par secondes et par jeton d'accès.
stats_detail_resume: Les statistiques sont disponibles sur 2 mois
stats_detail_description: Accédez au suivi des consommations des API
stats_detail_link: https://particulier.api.gouv.fr/stats
monitoring_link: https://status.api.gouv.fr/
monitoring_description: |
  La DINUM s’engage à ce que le Service soit accessible à 95% et la DINUM s’engage à améliorer progressivement ce rendement.
contact_link: api-particulier@api.gouv.fr
doc_tech_link: https://particulier.api.gouv.fr/api/open-api.yml
themes:
  - Particulier
visits_2019: 15831
uptime: 99.992 # https://uptimerobot.com/dashboard#777746216 * https://uptimerobot.com/dashboard#778826562 / 2
last_update: 31/03/2021
content_intro: |
  <External href="https://particulier.api.gouv.fr/">API Particulier</External> permet aux entités administratives d'accéder aux données administratives des particuliers, afin de simplifier leurs démarches.

  <Button href="https://particulier.api.gouv.fr/">Consulter le site API Particulier</Button>

---

  Ce bouquet de données provenant d'administrations différentes est utilisable :

  - dans le cadre des démarches en ligne proposées aux usagers (formulaires en ligne ou téléservices) ;
  - dans les logiciels métiers utilisés par les agents habilités en guichet.

  ### À quoi sert l’API Particulier ?
  
  L'API Particulier est un bouquet d'API donnant accès à des données administratives des particuliers : quotient familial CAF, composition familiale, statut demandeur d’emploi, statut élève scolarisé et élève boursier, statut étudiant et statut étudiant boursier.
  
  **L'accès à ces données par l'API Particulier permet de simplifier les démarches des particuliers** dans leur accès aux aides et aux services publics. Le calcul du tarif d'une carte de transport ou d'un abonnement des enfants à la cantine peut par exemple être fait automatiquement.
  
  ### API disponibles dans le bouquet API Particulier :

<Button href="https://particulier.api.gouv.fr/catalogue">Consulter le catalogue des API</Button>
  
  ### Ce qu'API Particulier change pour vous, administrations :

  **En tant qu'administration**, en intégrant la brique API Particulier dans votre système d’information ou votre site internet :

  - ✅ Vous n’avez **plus besoin de demander certaines informations** aux particuliers, comme le certificat de scolarité ou l'attestation CAF ;

  - ✅ Vous n’avez **pas de saisie ou de vérification** supplémentaire à réaliser ; 
  
  - ✅ les **informations sont certifiées** ;

  - ✅ Vous accédez avec une seule habilitation aux **données de différents fournisseurs** : la Caisse nationale des allocations familiales (CNAF), la sécurité sociale agricole (MSA), Pôle emploi, le ministère de l'enseignement supérieur et de la recherche (MESR), le ministère de l'éduction nationale (MEN) et enfin le Centre national des œuvres universitaires et scolaires (Cnous).

  ### C'est aussi plus simple pour vos usagers :

  - ✅ Leur démarche est réalisable 100% en ligne autant qu'en guichet ;

  - ✅ Ils n'ont plus besoin de rassembler et saisir les informations ou documents déjà connus de l'administration.

  ⚠️ Les données de l’API ne permettent pas encore de calculer les tarifs en établissement d'accueil du jeune enfant (crèche, multi-accueil, halte-garderie…). **Elles ne doivent donc pas être utilisées pour le calcul des participations familiales en Eaje.**

---

## API accessibles depuis l'API Particulier

  | API | Fournisseur des données | Données | Disponibilité sur API Particulier |
  |---------------------|----------|------------------------------------- |------------------- |
  | **Quotient familial CAF** | CNAF | Quotient familial CAF, composition familiale<br>[📖 Documentation](https://particulier.api.gouv.fr/catalogue/cnaf/quotient_familial) | ✅                      |
  | **Statut étudiant** | MESR | Statut, établissement<br>[📖 Documentation](https://particulier.api.gouv.fr/catalogue/mesr/statut_etudiant) | ✅                      |
  | **Statut étudiant boursier** | Cnous | Statut, niveau de bourse<br>[📖 Documentation](https://particulier.api.gouv.fr/catalogue/mesr/cnous/statut_etudiant_boursier)      | ✅      |
  | **Statut demandeur d'emploi** | Pôle Emploi |Statut et catégorie (A,B,C,D)<br>[📖 Documentation](https://particulier.api.gouv.fr/catalogue/pole_emploi/situation)     | ✅          |
  | **Statut élève scolarisé**   | Ministère de l'éducation nationale| Attestation de scolarité et statut boursier |T2 2023    |
  | **Indemnités demandeur d'emploi** | Pôle Emploi | Montants et types d'indemnisations | T2 2023               |
  | **Statut Complémentaire santé solidaire (CSS)**              |  Direction de la sécurité sociale | Indique si le particulier a la CSS, avec ou sans participation. | T2 2023               |
  | **Statut Revenu de solidarité active (RSA)**                 |Direction de la sécurité sociale | _En cours de définition_| T4 2023               |


### Et si j'ai besoin d'une API France connectée ? <a name="api-france-connectees"></a>

Certaines API du bouquet API Particulier peuvent être utilisées avec FranceConnect :

  | API sur API Particulier | Utilisable avec FranceConnect depuis API Particulier | Alternatives |
  |------------------- |--------------------------- | ---------------- |
  | **Quotient familial CAF** - CNAF | ❌ _Calendrier prévu fin 2023_    | Pas d'alternative |
  | **Statut étudiant** - MESR |  ✅ Oui ! | / |
  | **Statut étudiant boursier** - Cnous   |  ✅ Oui ! | / |  
  | **Statut demandeur d'emploi** - Pôle Emploi | ❌ Non...  | Données disponibles avec FranceConnect depuis une autre API : ✅ [API statut demandeur d'emploi](/les-api/api-statut-demandeur-emploi)   |
  | **Indemnisation Pôle emploi** - Pôle Emploi | ❌ Non...  | Données disponibles avec FranceConnect depuis une autre API : ✅ [API indemnisation Pôle emploi](/les-api/api-indemnisation-pole-emploi)       |

🔎 En savoir plus sur [les API](https://api.gouv.fr/guides/api-definition) et les [API France Connectées](https://api.gouv.fr/guides/api-franceconnectees).


## Conditions générales d'utilisation

Les conditions générales d'utilisation sont disponibles à [ici en PDF](http://api.gouv.fr/resources/CGU%20API%20Particulier.pdf).

## Infolettre API Particulier

Chaque année, l'équipe de l'API Particulier envoie un bilan chiffré sur l'utilisation de l'API, et la feuille de route de l'année suivante (nouvelles démarches, prochaines données qui intègrent l'API...).

<Button href="https://487b4da0.sibforms.com/serve/MUIEADKIZQbixV2PoSlS2VU1cgnh4xihiaswOxPpI0HHRX4F9Wi2C8ojDtqpU70dpyEJF6s1JXYj0oHuHCHTpe-KKzm18PzpaKSBJ7Tq0yyz6FMst27i-kVe_gcvX-pK_rw_6DgRFukOX0HPq4gYVCkglTTjUslLjhGUva9aEN2m9O6CHjgYCuUND2QESrjEeviVzG_Z8Mq6WQwc">Abonnez-vous à l'infolettre API Particulier</Button>

## FAQ

<details>
  <summary>Qu'est-ce qu'une API ?</summary>

  Pour mieux comprendre ce qu'est une API, consulter cette [page](/guides/api-definition).

</details>

<details>
  <summary>Quelles sont les étapes pour utiliser l'API Particulier ?</summary>

  ### Je suis une collectivité ou une administration :

  1. **Je consulte [les cas d’usage de l'API Particulier](/les-api/api-particulier#exemples-d’application)** :
    - Si j'ai un éditeur de logiciel, je consulte le tableau en bas du cas d'usage pour savoir si mon éditeur intègre déjà l’API Particulier.
    - Sinon je contacte mon éditeur et je lui transmets le lien vers la documentation technique pour m'assurer qu'il peut intégrer l'API.
  2. **Je clique sur le bouton "[faire une demande d'habilitation](https://datapass.api.gouv.fr/api-particulier)"**, je crée mon compte DataPass ou je me connecte.
  3. **Une fois sur la première page du formulaire d'accès à l'API Particulier, je complète l'encadré "Qui implémentera l'API ?"** :
    - Si j'ai un éditeur, je coche "Votre éditeur de logiciel" et je le sélectionne dans la liste déroulante s'il est disponible.
    - Si je n'ai pas d'éditeur, je coche "Votre équipe de développeurs". Je clique sur "Suivant".
  4. **À la page suivante, rubrique "Modèles pré-remplis", je sélectionne le formulaire pré-rempli adéquat** :
    - Si j'ai un éditeur, je retrouve son nom et le nom de la solution dans la liste déroulante.
    - Si je n'ai pas d'éditeur, je laisse le mode par défaut "Demande libre".
  5. **Je complète mon formulaire** : informations sur le projet, données nécessaires, traitement des données, cadre juridique - dont délibération -, coordonnées de l'équipe dont responsable technique, délégué à la protection des données et responsable de traitement.
  6. **Une fois ma demande instruite et validée par l'équipe API Particuliere**, je reçois un e-mail m'indiquant où récupérer mon jeton. Je le transmets à mon éditeur ou à mes développeurs.

  ### Je suis un éditeur et je ne suis pas encore référencé :

  ℹ️ Si vous êtes **éditeur de logiciels, c'est à votre client public, collectivité ou administration, de faire sa demande d'habilitation auprès de l'API Particulier**.

  Vous pouvez nous demander de vous référencer sur un cas d'usage afin de proposer un formulaire pré-rempli qui simplifiera l'expérience de vos clients. Voici la procédure à suivre :

  - Je repère les données dont mes clients publics ont besoin pour un cas d'usage précis que je peux ou pourrai proposer dans ma solution logicielle ;
  - Je consulte la documentation technique, et j'utilise le bac à sable pour tester les appels d'API ;
  - J'écris à [cette adresse](https://api.gouv.fr/parcours-client?source=preFooter) pour être référencé sur le cas d'usage associé et avoir un formulaire pré-rempli à disposition de mes clients.
  
</details>

<details>
  <summary>Les API sur API Particulier sont-elles France connectées ?</summary>

L’API particulier n'est pas encore France connectée, de fait, même si votre service intègre le bouton France Connect, les informations de vos usagers nécessaires à l'appel de l'API (comme par exemple le numéro d'allocataire ou la date de naissance) et détenues dans l'identifiant France connect, devront transiter dans vos systèmes.

En revanche, certaines données présentes dans le bouquet API Particulier sont aussi accessibles par une version France connectée des API. Il vous faudra alors faire une demande d'accès auprès de ces API directement. La liste des alternatives France connectée est décrite [plus haut, à cette rubrique](#api-france-connectees).

🔎 En savoir plus sur les [API France Connectées](/guides/api-franceconnectees).

</details>


<details>
  <summary>Comment tester l'API ? Un jeton d'accès est-il nécessaire pour accéder au bac à sable ?</summary>

Vous pouvez accéder au [bac à sable](/documentation/api-particulier) afin de tester des appels d’API avec des données virtuelles. Aucune habilitation n’est nécessaire, un token est généré immédiatement.

**Il est possible d'ajouter des données au bac à sable à travers la plateforme Airtable :**
Depuis le [swagger](/documentation/api-particulier), en cliquant sur le détail des données proposées par un fournisseur de données, vous pouvez cliquer sur la liste des données présentes en bac à sable. Sur AirTable vous pouvez ensuite éditer des données.
Exemple [ici](https://airtable.com/appMEKRGMNrw4YRff) avec les données bac à sable de l'API de la CNAF.

</details>

<details>
  <summary>Comment récupérer mon jeton d'accès (token) une fois ma demande validée ?</summary>

1. **Une fois votre demande d'habilitation validée, un e-mail vous est envoyé** avec un lien vers [mon.portail-test-staging.api.gouv.fr/](https://mon.portail-test-staging.api.gouv.fr/).

2. **Une fenêtre de connexion (compte Datapass) s'ouvre**. Renseignez les mêmes identifiants utilisés lors de votre demande d'habilitation.

3. Sur votre espace [mon.portail-test-staging.api.gouv.fr/](https://mon.portail-test-staging.api.gouv.fr/), **votre jeton est disponible et peut-être copié**.
<br>⚠️ **Votre token vous est propre, il ne faut pas le diffuser.**  Vous ne devez jamais copier-coller un token dans un moteur de recherche ou dans un e-mail. L’usage de votre token se fait uniquement dans votre logiciel métier sécurisé utilisé pour réaliser vos appels.

4. **Vous devez transmettre ce jeton à votre éditeur ? Ou à votre équipe technique ?** Utilisez un moyen de transmission sécurisé (messagerie cryptée par exemple).

</details>
  
## Support utilisateur
 
Vous êtes utilisateur de l'API Particulier, vous rencontrez un problème et avez besoin d'échanger avec nous en transmettant des données sensibles ? Utilisez le [formulaire de transfert d'informations sécurisées](https://www.demarches-simplifiees.fr/commencer/api-particulier-transfert-securise-d-informations).

