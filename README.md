# cours_ISEN_LaTeX
alut
Package exemple pour créer un cours en LaTeX formaté pour l'ISEN Brest

## Procédure pour une utilisation "out-of-the-box"
Si vous voulez rapidement utiliser tout ceci, voici une liste des logiciels à installer (dans l'ordre). A la fin de cette liste, vous ouvrez le logiciel et vous appuyez sur Ctrl+Alt+b pour compiler.
  * https://atom.io
  * https://www.tug.org/texlive/
  * Ouvrez Atom text puis :
    * Edit->Preferences->Install
    * Tapez 'latex' et installez le package nommé latex
  * Redémarrez Atom, lorsque vous êtes sur un fichier .tex, appuyez sur Ctrl+Alt+b pour compiler.

## Utilisation
  * Les fichiers sources peuvent êtres compilés par le makefile
  * ou bien avec latexmk (produit des fichiers auxiliaires dans le dossier racine sauf si configuration de l'Output Directory dans les preferences du package latex)
