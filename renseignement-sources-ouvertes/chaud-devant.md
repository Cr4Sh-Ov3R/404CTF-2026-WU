****
**Catégorie**: OSINT - **Difficulté**: Intro 
# Chaud Devant

****

***Synopsis*** :
  > Derrière une mort spectaculaire se cache parfois une grande scientifique... Une fois que vous l'aurez retrouvée, un petit voyage en ligne vous permettra d'en savoir plus sur elle. 
  
  > Dans l'ordre, il vous faudra retrouver :

  > - L'année de décès
  > - le mont où elle est décédée,
  > - son nom de famille,
  > - son jour de naissance
  > - et le mois de naissance de son mari.

  > ressource fournie : cimetiere.jpeg

  > Format du flag : 404CTF{2026_Everest_Curie_01_01}


<p align="center">
<img alt="Screen Chall OSINT - Intro - Chaud Devant Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/chaud-devant-brief.png">
</p>


****

## Recherches

J'ai tout d'abord vérifié les données exif de la photo afin de vérifier si je n'avais pas d'info pertinente sur la localisation.

  - Pas de Géo-localisation
  - Date de la photo 28/02/2025

Je tente donc une recherche inversée avec Google Lens qui me mène au cimetière de Pfastatt, dans le Haut-Rhin en Alsace [site Findagrave.com](https://fr.findagrave.com/cemetery/2801783/cimeti%C3%A8re)

<p align="center">
<img alt="Ressource Chall OSINT - Intro - Chaud Devant Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/chaud-devant-cimetiere.jpeg">
</p>

Partant du principe que l'énoncé nous indique que nous recherchons une grande scientifique, je me dirige dans l'onglet des mémoriaux du site (ressorti en premier lors de la recherche de la photo en correspondance parfaite) et parcours brièvement la liste.

Je remarque dans la liste 2 personnes du même nom ayant une date de décès commune "Catherine Joséphine “Katia” Conrad Krafft" et "Maurice Paul Krafft" et indiquant que le monument est au cimetière de Pfastatt. D'autres part ces noms m'interrogent car il me semble en avoir déjà entendu parlé.

Je décide donc d'effectuer une recherche sur la femme, "Catherine Joséphine “Katia” Conrad Krafft" qui me ressort la fiche d'une grande vulcanologue française, née le le 17 avril 1942 à Soultz-Haut-Rhin (Haut-Rhin, Alsace) (ce qui peut être pertinent avec le cimetière de Pfastatt) et décédée avec son mari "Maurice Paul Krafft" lors d'une éruption sur le Mont Unzen, au Japon le 3 Juin 1991.

## Flag
Ces informations me permettent donc de tester le flag 

<p align="center">
<img alt="Screen flag Chall OSINT - Intro - Chaud Devant Chall" src="https://github.com/Cr4Sh-Ov3R/404CTF-2026-WU/blob/main/assets/osint/chaud-devant-flag.png">
</p>

<details>
<summary>Voir le flag :</summary>
FLAG : 404CTF{1991_Unzen_Krafft_17_03}
</details>


