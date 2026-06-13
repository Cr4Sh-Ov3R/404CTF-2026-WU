****
**Catégorie**: OSINT - **Difficulté**: Medium 
# Metro OSINT Dodo

****

***Synopsis*** :
  > Il y a quelques mois, en fin de matinée, j’ai mis plus d’une demie heure à faire un trajet direct qui normalement prend 11 à 12 minutes. Tout ça à cause d’un malaise voyageur à Châtelet. Mon trajet était entre deux stations comportant des noms de scientifiques.

  > Quelles étaient ces deux stations ?

  > Format du flag : 404CTF{les-halles_republique}


<p align="center">
<img alt="Screen Chall OSINT - Medium - Metro OSINT Dodo Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/metro_osint_dodo-brief.png">
</p>


****

## Recherches

Je décide tout d'abord de lister les lignes passant par Châtelet, en privilégiant le métro au vu du titre du chall, en prenant également en compte le "trajet direct de 11 à 12 min" évoqué dans l'énoncé.

Nous avons donc les lignes : 1, 4, 7, 11, 14

Je me rends compte que la ligne 7, contient pas mal de noms de scientifiques :
  - Pierre et Marie Curie, couple célèbre de physicien et détenteur du prix Nobel de physique en 1903 (avec Henri Becquerel) pour la découverte de la radioactivité naturelle. Connus de toutes et toutes mais au cas où [Musée Curie](https://musee.curie.fr/decouvrir/la-famille-curie/un-couple-de-pionniers)

  - Jussieu, qui tient visiblement son nom de sa proximité avec la place Jussieu mais également pour rendre hommage à Antoine-Laurent de Jussieu (1748-1836), membre de l'Académie des Sciences et professeur de botanique au Muséum national d'histoire naturelle.

  - Censier *Daubenton*, qui rend hommage à Louis Jean-Marie Daubenton (1716-1799), Médecin et naturaliste, pionnier dans le domaine de l'anatomie comparée [Biblothèque Nationale de France](https://data.bnf.fr/fr/ark:/12148/cb119993430)

  - Place Monge, qui tient son nom de la Place Monge et de la rue Monge, elles-mêmes bâptisées ainsi en hommage à Gaspard Monge (1746-1818), célèbre mathématicien français, inventeur de la géométrie descriptive, fondateur de l'École polytechnique et contributeur clé à la création de l'École Normale Supérieure. [Structurae](https://structurae.net/fr/ouvrages/station-de-metro-place-monge)

Bien que ces recherches m'aient appris beaucoup de choses intéressantes dans lesquelles je me suis "perdu" par curiosité, elles ont été infructueuses, je me suis donc concentré sur les autres lignes jusqu'à me concentrer sur la ligne 4 : 

  - Réaumur Sébastopol : en lien avec les noms des rues se croisant au dessus de la station et nous menant à René-Antoine Ferchault de Réaumur (1683-1757), chimiste, physicien et naturaliste français. Il est l'inventeur du thermomètre à alcool [Structurae](https://structurae.net/fr/ouvrages/station-de-metro-reaumur-sebastopol)

  - Montparnasse-Bienvenüe : En retraçant l'origine du nom, il s'avère que cette station tient son nom de la gare Montparnasse et rend hommage à Fulgence Bienvenüe (1852-1936), ingénieur Français et père du métropolitain, issus de l'école polytechnique ainsi que de l'école nationale des ponts et chaussées. [RATP.fr](https://www.ratp.fr/decouvrir/coulisses/au-quotidien/un-jour-une-station-montparnasse-bienvenue)

  Ces stations semblent correspondre à l'énoncé, à savoir, un trajet direct, des stations comportant des noms de scientifiques ainsi que d'un temps de trajets de 11min en fin de matinée d'après [Bonjour RATP](https://www.bonjour-ratp.fr/itineraires/reaumur-sebastopol/gare-montparnasse/)


<p align="center">
<img alt="Screen Plan métro Chall OSINT - Medium - Metro OSINT Dodo Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/metro_osint_dodo-plan.png">
</p>

## Flag 

  > Bien que ce soit les bonnes réponses, j'ai tenté le flag dans les 2 sens de circulation mais il s'avère que j'ai du faire une typo car je n'ai pas flag. J'ai bien flingué mes stats avec ce chall car j'en ai essayé pas mal de solutions potentielles jusqu'à arrêter ne trouvant pas la réponse
  > Ce n'est qu'en vérifiant à la fin du 404CTF avec les WU des autres participants que j'ai vu que c'était pourtant la bonne réponse et ça a flag. Je pense donc sincèrement à une typo quand j'ai tenté.

<details>
<summary>Voir le flag :</summary>
FLAG : 404CTF{reaumur-sebastopol_montparnasse-bienvenue}
</details>
