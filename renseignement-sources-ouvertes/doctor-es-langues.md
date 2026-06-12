****
**Catégorie**: OSINT - **Difficulté**: Facile 
# Doctor Es Langues

****

***Synopsis*** :
  > En farfouillant bien, vous devriez trouver le petit compte d'un chercheur qui utilise cette image en bannière. En étudiant son CV, vous trouverez qu'il maîtrise une langue à un niveau "confirmé”. Quelle est cette langue ?

  > Règle d'or en OSINT, n'interagissez PAS avec les personnes qui font l'objet de vos recherches. Ce n'est pas nécessaire.

  > Ressource fournie : banniere.jpg

  > Format du flag : 404CTF{klingon}


<p align="center">
<img alt="Screen Chall OSINT - Facile - Doctor Es Langues Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/doctor_es_langues-brief.png">
</p>


****

## Recherches

Je vérifie tout d'abord si je peux récupérer des infos intéressantes dans les données exif du fichier fourni et il s'avère que c'est plutôt intéressant. Je tombe sur l'information :

```bash 
"Image Description : Image de banniere Twitter de SadiQuatrenot"
```

<p align="center">
<img alt="Screen données exif Chall OSINT - Facile - Doctor Es Langues Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/doctor_es_langues-exiftool_banniere.png">
</p>

Ce qui nous donne effectivement un compte existant [@SadiQuatrenot](https://x.com/SadiQuatrenot) avec cette bannière et sur lequel est mentionné : *"Chercheur sur le climat. Fan de snorkeling et de photographie."*

<p align="center">
<img alt="Screen X.com SadiQuatrenot Chall OSINT - Facile - Doctor Es Langues Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/doctor_es_langues-compte-twitter-SadiQuatrenot.png">
</p>

En déroulant un peu le fil d'actu et en parcourant les médias liés au compte on peut trouver le CV de cette personne ainsi qu'un commentaire, redirigeant vers un blog *"blogger.com/profile/15995011235130208479"*

Blog sur lequel on retrouve le même CV ainsi que la mention *"Edit : j'ai fait quelques typos et oublis sur mon CV précédent, le voilà corrigé ^^"*

Un petit tour sur la Wayback machine pour voir si un fichier ou une publication antérieure aurait été scannée et on retrouve une archive du 7/05/2026 avec l'ancien CV sur lequel on retrouve une ligne dans les formations avec l'intitulé *"Apprentissage intensif du malais pendant 4 mois"

<p align="center">
<img alt="Screen Wayback Machine CV Chall OSINT - Facile - Doctor Es Langues Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/doctor_es_langues-wayback_machine-blogpost_CV.png">
</p>

## Flag

Le malais est une langue éthnique du peuple malais et originaire de l'Est de Sumatra en Indonésie et également parlée dans ses régions côtières voisines telles que les îles Riau, les îles Singapour et l'isthme de Kra [src : Wiki voyage](https://fr.wikivoyage.org/wiki/Guide_linguistique_malais)

> Pour les curieux [Asialyst.com](https://asialyst.com/fr/2025/07/10/langue-malaise-coeur-asie-sud-est/)

<p align="center">
<img alt="Screen flag Chall OSINT - Facile - Doctor Es Langues Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/doctor_es_langues-flag.png">
</p>

<details>
<summary>Voir le flag :</summary>
FLAG : 404CTF{malais}
</details>