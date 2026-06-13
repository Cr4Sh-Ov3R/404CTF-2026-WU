****
**Catégorie**: Divers - **Difficulté**: Intro 
# Super enQuête Libre 1/4

****

***Synopsis*** :
  > Vous êtes un enquêteur mandaté par Télématique NordRouan, une école réputée dans le domaine de la poterie, pour élucider une affaire de vol. Des pièces d’une valeur inestimable ont disparu et il est impératif de retrouver le coupable, sous peine de voir l’établissement fermer ses portes.

  > Pour mener votre enquête, vous obtenez l’accès à une base de données recensant l’ensemble des étudiants, professeurs et employés de l’école. Avant de vous confier l’affaire, l’école souhaite évaluer vos compétences. 
  
  > Votre première mission : déterminer quel badge Noel Laurent utilise actuellement. 

  > Format du flag : 404CTF{19}

  > nc spawn.404ctf.fr 10401


<p align="center">
<img alt="Screen Chall OSINT - Facile - Canular Savant 1/3 Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/divers/canular-savant-1-brief.png">
</p>


****

## Process 

En se connectant à la machine on peut constater qu'il existe les commandes .help et .quit qui nous sont proposées sur la base de donnée, je décide donc de lancer le .help afin de voir mes possibilités sur le système.

<p align="center">
<img alt="Screen Chall Divers - Intro - Super enQuête Libre 1/4 Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/divers/super_enquete_libre_1-brief.png">
</p>

```bash 
sql > .help
    Commandes spéciales
    .help
    .tables
    .schema [TABLE]
    .quit
```

Voyons donc les tables disponibles.

<p align="center">
<img alt="Screen .tables request Chall Divers - Intro - Super enQuête Libre 1/4 Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/divers/super_enquete_libre_1-tables.png">
</p>

La table Person me semble cohérente pour au vu de l'énoncé, et décide de vérifier le schéma afin de lancer une requête

<p align="center">
<img alt="Screen schema Person Chall Divers - Intro - Super enQuête Libre 1/4 Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/divers/super_enquete_libre_1-schema-Person.png">
</p>

Sachant que nous recherchons le badge actuellement utilisé par NOEL Laurent, on lance la requête en fonction du *last_name* me disant qu'il n'y en aurait probablement pas énormément.

<p align="center">
<img alt="Screen SQL request last_name Chall Divers - Intro - Super enQuête Libre 1/4 Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/divers/super_enquete_libre_1-SQL-request-last_name.png">
</p>

La requête nous donne un Noel Laurent portant un *person_id:38*, je lance donc la recherche dans la table Badge avec le *person_id* correspondant, ce qui me donne 2 badges pour cette personne dont le dernier en date porte le *badge_id:165*

<p align="center">
<img alt="Screen SQL request id Chall Divers - Intro - Super enQuête Libre 1/4 Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/divers/super_enquete_libre_1-SQL-request-id.png">
</p>

## Flag

<details>
<summary>Voir le flag :</summary>
FLAG : 404CTF{165}
</details>
