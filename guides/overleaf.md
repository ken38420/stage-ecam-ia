# Compiler ton CV et ta lettre sur Overleaf

[Overleaf](https://www.overleaf.com) est un éditeur LaTeX en ligne et gratuit. Rien à installer.

1. Crée un compte (l'adresse de l'école marche).
2. **New Project** → **Blank Project** → nomme-le, ex. `CV_Airbus_Methodes`.
3. Ouvre `main.tex`, efface tout et colle le code `.tex` donné par l'IA (du `\documentclass` au `\end{document}`).
4. Clique sur **Recompile**. Le PDF s'affiche à droite.
5. Vérifie : **une seule page**, pas de mot coupé, bon nom d'entreprise et bon intitulé.
6. Télécharge le PDF (icône de téléchargement au-dessus de l'aperçu) et renomme-le `CV_Prénom_NOM_Intitulé_Entreprise.pdf`.

Refais la même chose dans un second projet pour la lettre.

## Problèmes fréquents
- **Erreur rouge à la compilation** : copie le message d'erreur à l'IA, elle corrige le code.
- **Le CV fait 2 pages** : demande à l'IA « le CV déborde sur 2 pages, coupe du contenu sans tasser ».
- **Accents bizarres** : vérifie dans Menu → Settings que le compilateur est **pdfLaTeX**.
- **Astuce** : garde un projet Overleaf par candidature pour retrouver et réutiliser tes versions.

## Test ATS
Ouvre le PDF, fais Ctrl+A puis colle le texte dans un bloc-notes. Si le texte sort propre et dans l'ordre, les logiciels de recrutement le liront.
