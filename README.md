# stage-ecam-ia 🎓

**Passe les filtres ATS et décroche plus d'entretiens pour ton stage de fin d'études, sans rien inventer.**

Un kit pour les élèves de l'ECAM LaSalle, utilisable avec n'importe quelle IA (ChatGPT, Gemini, Claude, Mistral…). Tu donnes ton CV et ta coloration, et en deux échanges l'IA connaît ton profil. Ensuite, pour chaque offre, elle :

- extrait les **mots-clés ATS** à l'orthographe exacte de l'offre et donne un score de correspondance honnête ;
- écrit un **CV une page** titré comme l'offre, avec les mots-clés placés là où les ATS les comptent ;
- vérifie la **couverture ATS** du CV final (mots-clés présents ou absents, avec la raison) ;
- rédige une **lettre** factuelle, avec une preuve réelle pour chaque exigence ;
- prépare tes **entretiens** et tes **relances**, et suit ton **taux candidature → entretien**.

Livraison en **LaTeX** (à compiler sur Overleaf, gratuit) ou en **PDF**, au choix.

---

## 🚀 Démarrage

1. **Télécharge le dépôt** : bouton vert `Code` → `Download ZIP`, puis dézippe.
2. Dans ton IA, crée un espace avec instructions et fichiers. Guides :
   [ChatGPT](guides/chatgpt.md) · [Gemini](guides/gemini.md) · [Claude](guides/claude.md) · [Autres IA](guides/autres-ia.md)
3. Colle **`PROMPT.md`** dans les instructions.
4. Ajoute les fichiers de **`fichiers/`** et **`modeles/`**.
5. Écris **« Commence l'onboarding »** :
   - **1er échange** : tu envoies ton CV et tu indiques le format (LaTeX ou PDF), ta coloration, tes dates et les métiers visés ;
   - **2e échange** : tu coches dans la liste de ta coloration ce que tu as vraiment fait (cours ou projet).
   C'est tout : l'IA remplit ton profil et te sort un CV générique par métier visé.
6. Colle une offre complète (missions + profil recherché) et c'est parti.

> Pas d'espace « projet » dans ton IA ? Colle `PROMPT.md` en premier message et joins les fichiers. Refais-le avec tes fichiers à jour à chaque nouvelle conversation.

---

## 📁 Contenu

```
stage-ecam-ia/
├── PROMPT.md                      ← instructions à coller dans l'IA
├── fichiers/
│   ├── colorations_ecam.md        ← mots-clés + liste à cocher par coloration / pathway
│   ├── profil_candidat.md         ← ton profil (rempli à l'onboarding)
│   ├── methode_candidature.md     ← méthode détaillée + mots-clés par secteur
│   ├── regles_ats.md              ← règles de lisibilité ATS
│   └── historique_candidatures.md ← suivi + taux candidature → entretien
├── modeles/
│   ├── modele_CV.tex              ← CV une page compatible ATS
│   └── modele_LM.tex              ← lettre une page
└── guides/                        ← mise en place par IA + Overleaf
```

## 🎯 Colorations couvertes

**Arts et Métiers** : Matériaux et Structures Avancées · Advanced Software and Hardware · Transition Énergétique · Usine du Futur · Énergies Renouvelables
**Engineering** : Robotics and Automation · Sustainable Energy · Mechanical Engineering · Industrial Engineering and Supply Chain

Le contenu des colorations vient d'un guide non officiel : **vérifie et corrige** `colorations_ecam.md` si le programme de ta promo est différent, et propose la correction au dépôt.

## ⚠️ Les règles qui font la différence

1. **Rien d'inventé.** Un mot-clé que tu ne peux pas défendre en entretien te fait perdre l'entretien. L'IA refuse et cherche ta preuve réelle la plus proche.
2. **Ne coche que ce que tu as fait.** Un élément au programme de ta coloration n'est pas une compétence tant que tu ne l'as pas pratiqué.
3. **Garde tes fichiers à jour.** Si ton IA ne peut pas les modifier, recopie le bloc « 📌 À COPIER DANS TES FICHIERS ».
4. **Relis avant d'envoyer** : entreprise, intitulé, dates.

## 🔒 Confidentialité

Dépôt **public** : ne pousse **jamais** ton CV, ton profil rempli ou tes candidatures. Le `.gitignore` exclut les PDF, les .docx et le dossier `mes_fichiers/`.

## 🤝 Contribuer

Programme de coloration à corriger, secteur à ajouter, IA testée : voir [CONTRIBUTING.md](CONTRIBUTING.md).

Built with Claude
