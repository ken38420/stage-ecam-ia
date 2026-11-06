# Méthode — Traitement d'une offre de stage

À appliquer **à chaque offre collée**. Données personnelles : `profil_candidat.md`. Lisibilité ATS : `regles_ats.md`.

---

## 0. Règle n°1 — Cohérence et vérité

Le but est de passer l'ATS **et** de tenir 45 minutes d'entretien technique. Tout mot ajouté doit pouvoir être défendu par un exemple réel.

**Autorisé**
- Reformuler une expérience réelle avec le vocabulaire exact de l'offre (ex. « calcul mécanique » → « justification structurale » si c'est bien ce qui a été fait).
- Mettre en avant une compétence déjà présente dans le profil, même secondaire.
- Ajouter la forme anglaise ou longue d'un sigle déjà maîtrisé : « AMDEC (FMEA) », « MSP (SPC) », « FEA / MEF ».

**Interdit**
- Inventer un outil, une norme, une certification ou un chiffre. Lean / Six Sigma suivis en cours = **formation**, jamais « Green Belt » ni « certifié ».
- Présenter un cours comme une expérience professionnelle, ou une association étudiante comme une entreprise (toujours « (association étudiante) »).
- Surévaluer un rôle : préférer « contribution à », « coordination du sous-système » à « pilotage du projet » si la personne n'était pas cheffe de projet.
- Texte caché, mots-clés en blanc, liste de mots-clés sans contexte : pénalisé par les ATS et par les recruteurs.

**Compétences adjacentes** (outils classiques du domaine absents du profil) : ne jamais les ajouter d'office. Les poser dans « À valider » : « As-tu déjà utilisé X ? jamais / en cours / en projet / en entreprise ». Vérifier d'abord `profil_candidat.md` : ne jamais redemander une info déjà confirmée.

**Chiffres** : uniquement ceux du profil. Sinon, marqueur `[À COMPLÉTER : ...]` dans la lettre plutôt qu'inventer.

---

## 0 bis. Règle n°2 — CV sobre et aéré

Un RH parcourt un CV en quelques secondes : garder l'essentiel.

- **Zéro doublon** : une info (outil, méthode) apparaît une seule fois, ou deux au maximum (une preuve en expérience + la ligne Compétences).
- **Formation** : 2 lignes par école (nom + diplôme + dates / spécialisation + lieu). Au plus 1 bullet, uniquement pour un projet directement lié à l'offre. Pas de liste de cours.
- **Expériences** : 3 à 5, les plus pertinentes en premier ; une expérience moins liée passe en dernier avec 1 bullet court. **1 à 2 bullets par expérience, 1 ligne chacun.**
- **Compétences** : 3 à 4 lignes courtes, 5 à 6 éléments par ligne max, sans parenthèses explicatives.
- **Centres d'intérêt** : une ligne par activité. L'argumentaire va dans la lettre.
- **Mise en forme** : police 11 pt, marges ~0,75 in, gras sur 1 à 2 mots-clés par bullet maximum.
- **La page A4 est remplie jusqu'en bas**, mais sans tasser. Si le CV dépasse, couper du contenu.

---

## 1. Format de réponse pour chaque offre

Sans préambule, dans cet ordre :

### A. Analyse express (≤ 10 lignes)
- Poste / entreprise / secteur / lieu / langue de l'offre / dates.
- **Mots-clés ATS** (8 à 15) à l'orthographe exacte de l'offre : hard skills · outils · normes/méthodes · soft skills.
- Matching : ✅ couvert · 🟡 adjacent (à valider) · ❌ absent (ne pas ajouter, préparer une réponse d'entretien).
- Score de correspondance (/10), honnête, en une ligne.

### B. CV de départ
Le CV déjà produit le plus proche (CV générique ou candidature précédente du même secteur, voir `historique_candidatures.md`), sinon `modele_CV.tex` + une phrase de justification.

### C. CV
- Ligne de titre sous le nom, calquée sur l'intitulé de l'offre (§2).
- Bullets réécrits avec les mots-clés prioritaires **dans les expériences**.
- Ligne Compétences réordonnée : outils cités dans l'offre en premier.
- 1 page, LaTeX valide (`\&`, `\%`, `\_` échappés). Pas de `\\` juste avant `\begin{itemize}` (ligne vide qui fait déborder).

### D. Lettre de motivation
Voir §4, à partir de `modele_LM.tex`.

### E. Livrables
Selon le format choisi à l'onboarding : `.tex` complets prêts pour Overleaf, ou PDF compilés. 1 page chacun, vérifiés (pas de mot coupé dans l'objet, dates cohérentes).

### F. Message d'accompagnement
3 à 5 lignes, pour email ou LinkedIn.

### G. À valider (max 4 points)
Une compétence par question, réponse fermée.

### H. Compétences Workday (si candidature via myworkdayjobs)
10 à 15 termes courts, un par saisie, à l'orthographe la plus probable de l'autocomplétion (souvent anglais ou générique). Uniquement des compétences confirmées ; celles de l'offre en premier.

---

## 2. Règles ATS du CV

1. **Titre sous le nom**, dans les termes de l'offre :
   `Stage de fin d'études -- [Intitulé exact de l'offre]` puis `Disponible à partir de [mois année] -- [durée] mois`. C'est le levier ATS le plus fort.
2. **Correspondance exacte** : l'offre écrit « AMDEC » → « AMDEC » ; elle écrit « FMEA » → « AMDEC (FMEA) ». Idem « TRS / OEE », « FEA / MEF ».
3. **Densité naturelle** : mot-clé prioritaire 2 fois max (expérience + Compétences).
4. **Structure** : une colonne, sections standard (Formation, Expérience, Compétences), pas de tableau, pas d'icônes, rien en en-tête/pied de page.
5. **Établissements étrangers** : nom officiel + traduction, ex. « Politecnico di Milano (Polytechnique de Milan) ».
6. **Dates homogènes** : « Mois. AAAA -- Mois. AAAA », identiques dans tous les documents.
7. **Langue** : CV dans la langue de l'offre (sections Education, Experience, Skills en anglais).
8. **Export** pdfLaTeX (Overleaf : compilateur pdfLaTeX par défaut) avec, dans le préambule : `\input{glyphtounicode}` et `\pdfgentounicode=1` (déjà dans `modele_CV.tex`). Test : tout sélectionner dans le PDF, coller dans un bloc-notes ; si le texte sort propre et dans l'ordre, l'ATS le lira.

---

## 3. Banques de mots-clés par secteur

Légende : **[P]** prouvé par le profil, utilisable librement · **[A]** adjacent, uniquement après validation · **[V]** vocabulaire du secteur, pour la lettre uniquement, **jamais comme compétence revendiquée**.

Les [P] se construisent à partir de `profil_candidat.md`. Quand une question est tranchée, faire passer le terme de [A] à [P] (ou le noter « non pratiqué »).

### 3.1 Aéronautique / Spatial / Défense — calcul, conception, essais
- **[A] courants** : Nastran/Patran, HyperMesh, Abaqus, Ansys, CATIA V5, 3DEXPERIENCE, EN 9100, tolérance aux dommages, Python, CFD (Fluent, Star-CCM+), Part 21, MSA / R&R, calcul d'incertitudes (GUM), essais vibratoires / chocs.
- **[V]** navigabilité, certification (EASA), programme, sous-ensemble, allègement, qualification, bureau de calcul, stress engineer, Reserve Factor, ARP4754 / ARP4761, DAL, CS-25, FHA / SSA, Moyens de Conformité, AIT (Assemblage, Intégration et Test), MCI (masse, centrage, inertie).
- **Angle narratif** : une marge de sécurité se démontre, elle ne se suppose pas ; une mesure ne vaut que par son incertitude.

### 3.2 Amélioration continue / Qualité / Méthodes / Excellence opérationnelle
- **[A] courants** : Lean Manufacturing, 5S, Kaizen, TPM, SMED, TRS (OEE), VSM / VSA, PDCA, DMAIC, Six Sigma, MSP/SPC, AMDEC (FMEA), 8D, QRQC, Ishikawa, 5 Pourquoi, Poka-Yoke, Kanban, chronoanalyse, Gemba, standard work, ISO 9001, IATF 16949, ISO 13485, Power BI, SAP, MES.
- **[V]** performance industrielle, flux, productivité, taux de rebut, non-conformités, terrain, goulot d'étranglement, cadence, routines d'amélioration, SQCDP, management visuel.
- **Angle narratif** : un chantier se construit avec ceux qui y travaillent, pas à leur place ; mesurer, analyser, corriger, recommencer.

### 3.3 Luxe (maroquinerie, horlogerie-joaillerie, parfums-cosmétiques, mode)
- **[A] courants** : qualité perçue, métrologie, BPF / ISO 22716, traçabilité, audit, MS Project, packaging, chaîne graphique / BAT, prototypage, impression 3D, rendu 3D, Rhino, Creo.
- **[V]** savoir-faire, métiers d'art, artisans, manufacture, ateliers, geste, finition, zéro défaut, préséries, nouveautés, flacon, étui, décor, homologation, développement durable / RSE.
- **Angle narratif** : améliorer un processus sans dénaturer le geste ; une tolérance a un sens fonctionnel.
- **Piège** : ne pas parler de « réduction des coûts » en premier ; parler qualité, fiabilité, standards. Chez Hermès, dire « rencontre » plutôt qu'« entretien ».

### 3.4 Conception produit / R&D / Mécanique / Bureau d'études
- **[A] courants** : CAO 3D (SolidWorks, CATIA, Creo, NX), plans 2D (AutoCAD), ISO GPS, tolérancement, chaînes de cotes, cahier des charges fonctionnel, analyse fonctionnelle, DFM/DFA, prototypage, PLM (Teamcenter, Windchill), RDM / FEA, choix matériaux et procédés.
- **[V]** cycle en V, revue de conception, industrialisation, dossier de définition, gel de conception.
- **Angle narratif** : un fichier qui part en fabrication doit être juste du premier coup ; une pièce mal pensée pour le montage revient toujours au bureau d'études.

### 3.5 Supply chain / Logistique / Contrôle de gestion industriel
- **[A] courants** : ERP (SAP MM/PP), WMS, S&OP, MRP, prévision de la demande, gestion des stocks, Excel (TCD, RECHERCHEV…), Power BI, Power Query, SQL, certification APICS/ASCM.
- **[V]** taux de service, couverture de stock, rupture, approvisionnement, flux amont/aval, lead time, valorisation des stocks, prix de revient, écarts budgétaires.
- **Angle narratif** : une décision de flux se prend sur la donnée, pas sur l'impression.

### 3.6 Ajouter un secteur
Quand une offre ouvre un nouveau secteur, créer une section 3.x avec [A] / [V] / angle narratif, et y ranger les [P] confirmés.

---

## 4. Lettre de motivation

**Format** : 250 à 350 mots, 4 à 6 paragraphes courts, une page. Objet : « Candidature, Stage [année], [intitulé exact], [entreprise], [lieu] » (+ référence si elle existe).

**Structure**
1. **Accroche (2-3 phrases)** : un fait précis et vérifiable (recherche web) sur le site, le produit ou l'enjeu du poste, relié à la mission. Jamais « Actuellement étudiant en… », jamais « C'est avec un grand intérêt… ».
2. **Preuves (paragraphe le plus long)** : les 2 ou 3 exigences principales de l'offre, chacune prouvée par une expérience concrète (contexte → action → résultat). Priorité : expériences en entreprise, puis projets réels / associations, puis formation.
3. **Ce qui manque, dit sobrement** : « Je n'ai encore jamais fait X : c'est ce que je viens apprendre. »
4. **Différenciation** : un centre d'intérêt relié explicitement à une exigence du poste, en une ou deux phrases.
5. **Clôture** : date de début et durée, écart éventuel avec l'offre, demande d'entretien sobre.

**Style**
- Phrases courtes, verbes d'action, 3 à 5 mots-clés de l'offre repris naturellement.
- La lettre explique **pourquoi** et **comment** ; le CV liste **quoi**.
- Interdits : « dynamique et motivé », « rigoureux et polyvalent » sans preuve, « je me permets de », « force de proposition », « véritable passion », superlatifs sur l'entreprise.
- Politesse : « Je vous prie d'agréer, Madame, Monsieur, l'expression de mes salutations distinguées. » Nom du recruteur s'il est connu.
- LaTeX : `~:` avant les deux-points pour éviter un « : » en début de ligne.

**Anglais** : cover letter de 250 à 300 mots, « Dear Hiring Manager », « Kind regards », niveau cohérent avec celui déclaré (la personne doit pouvoir la défendre à l'oral).

---

## 5. Checklist finale

- [ ] Chaque mot-clé est [P] ou validé.
- [ ] Le titre du CV reprend l'intitulé de l'offre.
- [ ] Les 5 mots-clés prioritaires sont dans le CV **et** la lettre.
- [ ] CV sobre : aucune info en double, 1 à 2 bullets courts par expérience.
- [ ] Rôles associatifs signalés, aucun rôle surévalué.
- [ ] Dates identiques CV / lettre / profil ; date de début et durée indiquées.
- [ ] CV et lettre : 1 page chacun, livrés dans le format choisi (.tex ou PDF).
- [ ] Lettre ≤ 350 mots, sans formule interdite, au moins 2 preuves concrètes.
- [ ] Ligne ajoutée dans `historique_candidatures.md`.
