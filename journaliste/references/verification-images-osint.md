# Vérification d'images, vidéos et OSINT

Une image ou une vidéo frappe l'œil et emporte la conviction : on croit ce que l'on voit. C'est précisément pour cela qu'un visuel n'est **jamais une preuve en soi**. Il peut être authentique mais sorti de son contexte, mis en scène, daté d'un autre moment, pris dans un autre pays — ou entièrement fabriqué par une intelligence artificielle. Le travail du journaliste n'est pas de juger si l'image « semble vraie », mais d'établir, par recoupement, **d'où elle vient, quand et où elle a été produite, et ce qu'elle montre réellement**. L'OSINT (*open source intelligence*, renseignement en sources ouvertes) désigne l'ensemble des techniques qui exploitent les données librement accessibles pour répondre à ces questions. Cette fiche en donne la méthode ; elle prolonge `references/verification-recoupement.md`, dont elle est un cas d'application au visuel.

## Pourquoi une image n'est jamais une preuve en soi

Trois mécanismes trompent indépendamment de toute retouche :

- **La recontextualisation** : une vraie image, authentique et non modifiée, est présentée comme illustrant un autre événement, un autre lieu ou une autre date. C'est la manipulation la plus fréquente, parce qu'elle ne laisse aucune trace technique : le fichier est intact, seul le récit ment.
- **La mise en scène** : la scène a été organisée, jouée ou rejouée pour la caméra. L'image est réelle mais l'événement qu'elle prétend documenter ne l'est pas.
- **La fabrication** : l'image est retouchée (montage, effacement, ajout) ou générée par IA. Voir plus bas et `references/ia-et-journalisme.md`.

Conséquence pratique : ne publie jamais un visuel sur sa seule apparence de vérité. Une image « choc » qui circule vite est, statistiquement, la plus suspecte — l'émotion qu'elle suscite est justement ce qui désactive la vigilance.

## La recherche d'image inversée

La recherche inversée part de l'image pour retrouver ses occurrences antérieures sur le web. Elle répond à deux questions décisives : **d'où vient ce visuel** et **depuis quand circule-t-il** ? Si une image présentée comme prise aujourd'hui existe en ligne depuis trois ans, la recontextualisation est démontrée.

- **Google Lens / images** : large couverture, bon pour les images très diffusées et la reconnaissance de lieux ou d'objets.
- **TinEye** : spécialisé dans l'antériorité ; classe les résultats par date d'apparition (« oldest »), utile pour remonter à la première publication.
- **Yandex** : souvent le plus performant sur les visages et les paysages, et sur l'espace post-soviétique.

Recoupe **plusieurs moteurs** : chacun indexe une part différente du web, aucun n'est exhaustif. Recadre l'image, isole un détail signifiant (une enseigne, un panneau, un visage) et relance la recherche : un sous-élément donne parfois des résultats que l'image entière masque.

**Exemple :** une photo de manifestation présentée comme « hier à Paris » apparaît, via TinEye, sur un site d'agence daté de deux ans plus tôt, légendée dans une autre ville. L'antériorité suffit à invalider la légende sans rien dire d'autre.

## Géolocalisation et chronolocalisation

**Géolocaliser**, c'est établir *où* une image a été prise, en confrontant les indices visuels à des références cartographiques. **Chronolocaliser**, c'est établir *quand*.

Pour le lieu, croise les indices du cliché avec des sources ouvertes :

- Panneaux, plaques, enseignes, langue, type de véhicules, architecture, végétation, relief.
- **Cartographie** : Google Maps / Street View, OpenStreetMap, Mapillary pour les vues au sol ; images satellites (Google Earth, et leurs historiques) pour les vues aériennes et l'évolution d'un site.
- Confronte l'alignement des bâtiments, la silhouette du relief, la position des points fixes (clochers, pylônes) à la carte jusqu'à la concordance.

Pour la date et l'heure, exploite des indices physiques :

- **Les ombres** : leur direction et leur longueur donnent l'heure et la saison (outils comme SunCalc, à partir d'une position connue).
- **La météo** : neige, pluie, état du ciel se recoupent avec les archives météorologiques du lieu.
- **Indices temporels** : affiches, état d'un chantier, feuillage, présence d'éléments datables (un modèle de voiture, une banderole d'événement).

La géolocalisation est souvent la preuve la plus solide, parce qu'elle est **reproductible** : un confrère doit pouvoir refaire la démonstration à partir des mêmes repères. Documente-la (captures annotées, coordonnées) pour la rendre opposable.

## Les métadonnées EXIF

Les métadonnées EXIF, intégrées par l'appareil au fichier, peuvent indiquer date, heure, modèle d'appareil et parfois coordonnées GPS. Utiles, mais à manier avec prudence :

- Les **réseaux sociaux les suppriment** quasi systématiquement à l'envoi (recompression). Une image récupérée sur une plateforme n'a, le plus souvent, plus d'EXIF exploitables.
- Elles sont **falsifiables** : une date ou une position EXIF se modifie en quelques secondes.

Conclusion : l'EXIF est un indice, jamais une preuve autonome. Travaille de préférence sur le **fichier original** obtenu de l'auteur, et ne fais jamais reposer une datation ou une localisation sur les seules métadonnées — confronte-les toujours aux indices visuels et au recoupement.

## Deepfakes et images générées par IA

Les images de synthèse et les *deepfakes* (vidéos où un visage ou une voix est substitué) ont franchi le seuil du réalisme courant. Quelques indices visuels persistent — mains et doigts incohérents, texte illisible en arrière-plan, asymétries de visage, bijoux ou dentition irréguliers, fonds qui « fondent », éclairages contradictoires — mais ils **disparaissent** au rythme des progrès techniques.

- Les **outils de détection automatique sont faillibles** : ils produisent faux positifs et faux négatifs, et un « score » de détection ne constitue pas une preuve publiable.
- Adopte le **principe de prudence** : l'absence d'indice de fabrication ne prouve pas l'authenticité, et un indice suspect ne prouve pas la falsification. La détection ne remplace jamais la traçabilité — remonter à la **source originale** reste la démarche décisive.
- Sur le cadre de traitement, les biais et l'usage de l'IA dans la chaîne de production, voir `references/ia-et-journalisme.md`.

## La méthode de débunkage en 5 questions

Face à tout visuel douteux, applique cette grille avant toute reprise. Tant qu'une réponse manque, le visuel n'est **pas vérifié** et ne se publie pas comme tel.

| # | Question | Comment y répondre |
|---|---|---|
| 1 | Quelle est la **source originale** ? | Recherche inversée (Google Lens, TinEye, Yandex), remonter au premier auteur et au premier post |
| 2 | Quelle **date** ? | Antériorité en recherche inversée, chronolocalisation (ombres, météo), EXIF avec réserve |
| 3 | Quel **lieu** ? | Géolocalisation : Street View, cartes, satellite, indices visuels |
| 4 | Quel **contexte** ? | Que montre réellement la scène ? Que dit la légende d'origine ? Mise en scène ? |
| 5 | A-t-elle été **modifiée** ? | Retouche, montage, recadrage, génération par IA — indices et recoupement |

La logique : une seule réponse négative ou incertaine suffit à bloquer la publication. Et même cinq réponses solides s'accompagnent d'une **mention transparente** de la méthode et des limites (voir `assets/checklist-publication.md`).

## Authentique ne veut pas dire publiable

Établir qu'une image est réelle, datée et localisée règle la question de l'**exactitude**, pas celle du **droit** ni de la **dignité**. Une photo parfaitement authentique peut rester non publiable :

- **Droit à l'image et vie privée.** Sur la voie publique, lors d'une manifestation ou d'un événement d'actualité, la diffusion est plus largement admise ; mais un visage identifiable, un mineur, une victime ou un lieu privé exigent en principe un **accord**, sauf intérêt public majeur mis en balance. Voir `references/droit-presse.md`.
- **Dignité.** Les images de victimes, de corps ou de personnes en détresse se manient avec retenue : l'intérêt informatif ne justifie pas le voyeurisme. Flouter, recadrer ou renoncer sont des options.
- **Droits de l'auteur.** Une image trouvée en ligne a un auteur : sa réutilisation suppose une autorisation ou un cadre légal (actualité, courte citation), et toujours un **crédit**.

Documente l'accord obtenu et la base sur laquelle tu publies — c'est aussi ce que vérifie la `assets/checklist-publication.md`.

## La vérification des vidéos

Une vidéo se vérifie comme une suite d'images, avec une exigence supplémentaire : la continuité.

- **Décompose en images-clés** : extrais des images fixes (captures aux moments significatifs ou *images-clés*) et applique-leur la recherche inversée et la géolocalisation.
- **Analyse image par image** : ralentis la lecture pour repérer coupes, sauts, raccords suspects, incohérences d'ombres ou de décor entre deux plans — signes d'un montage ou d'un assemblage de séquences hétérogènes.
- **Remonte à la version source** : la première mise en ligne, la plus longue et la moins recompressée, prime sur les extraits repartagés. Le **son** se vérifie aussi (désynchronisation, ambiance incohérente avec le lieu prétendu).
- Recoupe avec d'autres prises de vue du même événement : plusieurs angles concordants renforcent l'authenticité ; une scène qui n'existe que dans une seule vidéo isolée appelle la méfiance.

## Ressources et réseaux de référence

- **Bellingcat** : collectif pionnier de l'investigation en sources ouvertes ; publie enquêtes, guides et boîtes à outils OSINT.
- **AFP Factuel** : service de vérification de l'AFP, exemples concrets de débunkage géolocalisé et chronolocalisé en français.
- **GIJN** (*Global Investigative Journalism Network*) : réseau international qui mutualise méthodes, outils et formations d'enquête, y compris OSINT, en français.

Inspire-toi de leurs méthodologies et **publie la tienne** : une vérification d'image n'a de valeur que si elle est reproductible et documentée — voir `references/verification-recoupement.md`.

## Sources

- [AFP Factuel — vérification et débunkage](https://factuel.afp.com/)
- [Global Investigative Journalism Network (GIJN) — ressources en français](https://gijn.org/fr/)
- [Charte d'éthique professionnelle des journalistes (SNJ)](https://www.snj.fr/content/charte-d%C3%A9thique-professionnelle-des-journalistes)
- [Conseil de déontologie journalistique et de médiation (CDJM)](https://cdjm.org/)
- [Reporters sans frontières (RSF)](https://rsf.org/fr)
- [Commission de la carte d'identité des journalistes professionnels (CCIJP)](https://www.ccijp.net/)
- [Fédération internationale des journalistes (FIJ / IFJ)](https://www.ifj.org/fr)
