# IA générative et journalisme

L'intelligence artificielle générative bouleverse les rédactions, mais ne change rien à l'essentiel : **l'IA est un outil, jamais un journaliste**. Elle peut accélérer une tâche, jamais endosser une responsabilité. Or le journalisme repose précisément sur une responsabilité — celle d'avoir vérifié, recoupé, contextualisé et signé une information devant le public. Un modèle de langage ne vérifie rien : il produit du texte plausible, pas du texte vrai. Cette fiche explique pourquoi la responsabilité éditoriale et déontologique reste **entièrement humaine**, distingue les usages utiles des usages à risque, et pose les garde-fous indispensables.

## Le principe directeur : l'IA n'a pas de responsabilité éditoriale

- **Un outil ne répond de rien.** Quand une erreur est publiée, ce n'est jamais « l'IA » qui est responsable, mais la rédaction et le ou la journaliste signataire. Déléguer une tâche à une machine ne délègue pas la responsabilité ; au contraire, l'usage d'un outil faillible l'augmente. Voir `references/deontologie.md`.
- **Un modèle de langage optimise la vraisemblance, pas la véracité.** Il prédit le mot le plus probable, ce qui le rend brillant pour reformuler et catastrophique pour établir un fait. D'où le risque d'**affabulation** (souvent appelé « hallucination ») : citations inventées, dates fausses, sources fictives énoncées avec un aplomb total.
- **La déontologie ne se sous-traite pas.** Exactitude, recoupement, respect des personnes, protection des sources, distinction des faits et des commentaires : ces devoirs (Charte de Munich, 1971) restent intégralement à la charge de l'humain, quel que soit l'outil employé. Voir `references/deontologie.md`.

Retiens la règle d'or : **tout ce que l'IA produit est une hypothèse, pas une information.** Une hypothèse se vérifie avant publication, jamais l'inverse.

## Usages utiles : accélérer le travail, pas le remplacer

Bien encadrée, l'IA fait gagner un temps précieux sur des tâches **auxiliaires**, à condition que leur résultat soit toujours relu et contrôlé par un humain.

| Usage | Bénéfice | Vigilance |
| --- | --- | --- |
| Transcription d'entretiens | Gain de temps considérable sur le verbatim | Relire l'audio : les modèles déforment noms propres, chiffres, mots techniques |
| Traduction | Premier jet rapide d'un document étranger | Vérifier nuances et faux-sens avant de citer |
| Recherche documentaire | Défrichage d'un sujet, pistes de lecture | Ne jamais citer une référence sans l'avoir retrouvée à la source |
| Résumé d'un gros corpus | Survol de centaines de pages, rapports, jugements | Le résumé peut omettre ou inventer : revenir au document original |
| Idéation d'angles | Élargir les pistes, sortir d'un angle évident | L'angle reste un choix éditorial humain, pas une suggestion machine |
| Aide au traitement de données | Nettoyage, code d'analyse, repérage de tendances | Recontrôler les calculs ; une analyse non vérifiée n'est pas un fait |
| Datajournalisme : collecte (*scraping*), statistique, visualisation | Exploiter de grands jeux de données qu'on ne lirait pas à la main | Documenter source, méthode et périmètre ; rendre l'analyse **reproductible** ; un graphique produit sans contrôle de la logique peut être faux ; l'IA ne choisit jamais ce qui mérite d'être publié |

Le bon réflexe : l'IA produit un **brouillon de travail interne**, jamais un contenu prêt à publier. Voir `references/methodologie-enquete.md` pour l'intégration de ces outils dans une enquête.

## Usages à risque ou à proscrire sans contrôle humain

Certains usages ne sont pas « interdits » par nature, mais le **devenir** dès qu'ils échappent au contrôle humain. Les énoncer permet de poser la frontière clairement.

- **Publier un texte généré non vérifié.** C'est la faute majeure : on diffuse alors du plausible non recoupé sous une signature humaine. Tout fait, tout chiffre, tout nom doit être contrôlé à la source. Voir `references/verification-recoupement.md`.
- **Faire « générer » des citations.** Une citation se recueille auprès d'une personne réelle, jamais auprès d'un modèle. Demander à une IA de « trouver une citation » revient à fabriquer un faux : c'est le terrain d'élection de l'affabulation. Voir `references/interview.md`.
- **Diffuser des images, voix ou vidéos de synthèse sans les signaler.** Une illustration générée, une voix clonée, une reconstitution visuelle peuvent induire le public en erreur. Leur usage doit rester exceptionnel, justifié, et **toujours signalé explicitement** ; on ne fait jamais passer du synthétique pour du réel.
- **Inventer ou « illustrer » un témoignage.** Reconstituer une scène, un visage ou une ambiance par IA crée une preuve fictive. Le journalisme montre ce qui est, il ne simule pas ce qui aurait pu être.

Avant / Après :

- **Avant (à proscrire)** : « J'ai demandé au modèle de me résumer le jugement et d'en extraire les citations clés, que j'ai mises entre guillemets dans l'article. »
- **Après (correct)** : « J'ai utilisé le modèle pour repérer les passages pertinents du jugement, puis j'ai relu chaque extrait dans le texte original avant de le citer. »

## Les quatre garde-fous déontologiques

### 1. Vérification humaine systématique

Aucun fait issu d'une IA n'entre dans un article sans contrôle humain à la source. L'outil propose, le journaliste dispose — et engage seul sa responsabilité. La vérification n'est pas une formalité ajoutée : c'est le cœur du métier. Voir `references/verification-recoupement.md`.

### 2. Transparence envers le public

Quand le recours à l'IA est **significatif** (texte largement généré, illustration de synthèse, traduction intégrale publiée, analyse automatisée de données), le public doit pouvoir le savoir. La transparence n'est pas un aveu de faiblesse : elle entretient la confiance, qui est le capital du journalisme. À l'inverse, un usage marginal et purement instrumental (correction orthographique, transcription relue) n'appelle pas nécessairement de mention. La règle de proportionnalité s'apprécie au cas par cas, idéalement selon une charte interne.

### 3. Protection des sources et confidentialité

Ne verse **jamais** de données sensibles, de documents confidentiels ou d'éléments identifiant une source dans un outil tiers : ces contenus peuvent être conservés, réutilisés pour l'entraînement, voire exposés. Un nom de lanceur d'alerte saisi dans un service en ligne grand public est un nom potentiellement compromis. Cloisonne, anonymise, et privilégie des outils maîtrisés pour le sensible. Voir `references/protection-sources-securite.md`.

### 4. Respect du droit d'auteur et citation des sources

Une IA peut restituer du contenu protégé sans en indiquer l'origine. Ne présente jamais comme tien un texte recraché par un modèle ; remonte toujours à la source réelle d'une information et cite-la. Le plagiat reste un plagiat, qu'il soit humain ou assisté. Voir `references/droit-presse.md` pour le cadre du droit d'auteur et `references/ecriture-journalistique.md` pour l'attribution des sources.

## Lutter contre la désinformation et les deepfakes

L'IA n'est pas qu'un outil de production : c'est aussi une **arme de désinformation**. Images truquées, vidéos et voix de synthèse (deepfakes), faux comptes générant du texte à la chaîne brouillent la frontière entre vrai et faux. Le journaliste a ici un double rôle.

- **Ne pas être un relais.** Avant de reprendre une image ou une vidéo virale, vérifie son authenticité : recherche d'image inversée, analyse des métadonnées, repérage des incohérences visuelles, géolocalisation et datation. Voir `references/verification-images-osint.md`.
- **Devenir un rempart.** Expliquer au public comment repérer un contenu synthétique, signaler ce qui est généré, et documenter les opérations de manipulation relève désormais de la mission d'information. Des cellules de vérification (par exemple l'AFP Factuel) outillent ce travail.
- **Garder le doute méthodique.** Un contenu d'autant plus spectaculaire ou indignant appelle d'autant plus de prudence : c'est souvent le signe d'une fabrication conçue pour être partagée sans réflexion.

## Doter la rédaction d'une charte d'usage de l'IA

Les bonnes pratiques individuelles ne suffisent pas : une rédaction a besoin d'un cadre **écrit, collectif et opposable**. Une charte d'usage de l'IA précise ce qui est permis, encadré ou interdit, et garantit une ligne cohérente. Elle gagne à couvrir :

- les usages autorisés et ceux soumis à validation hiérarchique ;
- l'**interdiction de verser** données sensibles et éléments de sources dans des outils tiers ;
- les règles de **transparence** vis-à-vis du public et de signalement des contenus de synthèse ;
- l'obligation de vérification humaine et la chaîne de responsabilité éditoriale ;
- le choix et l'homologation des outils, ainsi que la formation des équipes.

Cette charte d'usage s'articule avec la charte rédactionnelle générale ; voir `assets/charte-redactionnelle.md`. Deux textes de référence l'inspirent : la **Charte de Paris sur l'IA et le journalisme** (Reporters sans frontières, 2023), qui énonce des principes déontologiques pour l'usage de l'IA dans l'information, et les **avis du CDJM** (Conseil de déontologie journalistique et de médiation), qui appliquent les principes déontologiques existants aux cas concrets liés à l'IA. L'esprit commun de ces textes : l'IA ne dispense d'aucun devoir, elle en ajoute.

## Sources

- [Charte de Paris sur l'IA et le journalisme — Reporters sans frontières](https://rsf.org/fr/charte-de-paris-sur-l-ia-et-le-journalisme)
- [Conseil de déontologie journalistique et de médiation (CDJM) — avis et IA](https://cdjm.org/)
- [Charte d'éthique professionnelle des journalistes (Charte de Munich) — SNJ](https://www.snj.fr/article/charte-d%C3%A9thique-professionnelle-des-journalistes-1086375069)
- [AFP Factuel — vérification et lutte contre la désinformation](https://factuel.afp.com/)
- [GIJN — guides sur l'IA, l'OSINT et la vérification](https://gijn.org/fr/)
- [Fédération internationale des journalistes (IFJ)](https://www.ifj.org/fr)
- [Commission de la carte d'identité des journalistes professionnels (CCIJP)](https://www.ccijp.net/)
- [Code de la propriété intellectuelle (droit d'auteur) — Légifrance](https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006069414/)
