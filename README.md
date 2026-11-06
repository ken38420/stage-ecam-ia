# stage-ecam-ia 🎓

**Trouve ton stage de fin d'études avec une IA, sans rien inventer.**

Un kit pour les élèves de l'ECAM LaSalle (et au-delà) : tu donnes ton CV, l'IA te pose les questions qui manquent, puis pour chaque offre elle :

- analyse l'offre (mots-clés ATS, correspondance avec ton profil, score sur 10) ;
- écrit un **CV une page** et une **lettre de motivation** sur mesure, en **LaTeX** ou en **PDF** ;
- prépare tes **entretiens**, tes **relances** et tes messages LinkedIn ;
- tient l'**historique** de tes candidatures.

Ça marche avec **ChatGPT, Gemini, Claude, Mistral Le Chat** ou toute IA qui accepte des instructions et des fichiers.

---

## 🚀 Démarrage en 5 minutes

1. **Télécharge le dépôt** : bouton vert `Code` → `Download ZIP`, puis dézippe.
2. Dans ton IA, crée un espace avec instructions et fichiers (Projet, GPT personnalisé, Gem…). Guides pas à pas :
   [ChatGPT](guides/chatgpt.md) · [Gemini](guides/gemini.md) · [Claude](guides/claude.md) · [Autres IA](guides/autres-ia.md)
3. Colle le contenu de **`PROMPT.md`** dans les instructions.
4. Ajoute les fichiers des dossiers **`fichiers/`** et **`modeles/`**, plus **ton CV**.
5. Écris : **« Commence l'onboarding »**. L'IA te demande d'abord le format voulu (LaTeX ou PDF), puis lit ton CV.

Ensuite : colle une offre complète (missions + profil recherché) et laisse-toi guider.

> Tu n'as pas d'espace « projet » dans ton IA ? Colle `PROMPT.md` en premier message d'une conversation et joins les fichiers. Ça marche aussi, il faut juste le refaire à chaque nouvelle conversation.

---

## 📁 Contenu

```
stage-ecam-ia/
├── PROMPT.md                      ← instructions à coller dans l'IA
├── fichiers/
│   ├── profil_candidat.md         ← ton profil (vide au départ, rempli par l'onboarding)
│   ├── methode_candidature.md     ← méthode détaillée + mots-clés par secteur
│   ├── regles_ats.md              ← règles de lisibilité par les logiciels de recrutement
│   └── historique_candidatures.md ← suivi de tes candidatures
├── modeles/
│   ├── modele_CV.tex              ← CV une page compatible ATS
│   └── modele_LM.tex              ← lettre de motivation une page
└── guides/                        ← mise en place par IA + Overleaf
```

## 🧾 LaTeX ou PDF ?

Tu choisis au début :
- **LaTeX** : l'IA te donne le code `.tex`, tu le colles sur [Overleaf](https://www.overleaf.com) (gratuit) et tu télécharges le PDF. Ça marche avec toutes les IA. → [guide Overleaf](guides/overleaf.md)
- **PDF** : l'IA te livre directement le PDF, à condition qu'elle sache exécuter du code et générer des fichiers. Sinon, elle te le dit et te propose LaTeX.

## ⚠️ Les règles qui font la différence

1. **Rien d'inventé.** Pas d'outil, de chiffre ou d'expérience que tu ne peux pas défendre en entretien. L'IA refuse et te propose ta preuve réelle la plus proche.
2. **Réponds franchement aux questions de validation** : jamais / en cours / en projet / en entreprise. L'IA enregistre la réponse pour ne plus la reposer.
3. **Garde tes fichiers à jour.** Si ton IA ne peut pas modifier les fichiers elle-même, elle termine par un bloc « 📌 À COPIER DANS TES FICHIERS » : recopie-le et remplace le fichier dans ton projet.
4. **Relis toujours** le CV et la lettre avant d'envoyer : nom de l'entreprise, intitulé, dates.

## 🔒 Confidentialité

Ce dépôt est **public**. Ne pousse **jamais** ton profil rempli, ton CV ou tes candidatures sur GitHub. Garde-les sur ton ordinateur et dans ton IA. Le `.gitignore` exclut déjà les PDF et le dossier `mes_fichiers/`.

## 🤝 Contribuer

Une banque de mots-clés à ajouter pour ton secteur, une IA testée, une règle à améliorer ? Voir [CONTRIBUTING.md](CONTRIBUTING.md).
