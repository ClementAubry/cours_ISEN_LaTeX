# cours_ISEN_LaTeX

Package exemple pour créer un cours en LaTeX formaté pour l'ISEN Brest

## Procédure pour une utilisation "out-of-the-box"
Si vous voulez rapidement utiliser tout ceci, voici une liste des logiciels à installer (dans l'ordre). A la fin de cette liste, vous ouvrez le logiciel et vous appuyez sur f7 pour compiler.
  * https://www.sublimetext.com/3
  * https://packagecontrol.io/installation
  * https://www.tug.org/texlive/
  * Ouvrez Sublime text puis : 
    * Appuyez sur Ctrl+Shift+P
    * Une fenêtre s'ouvre, commencez à taper Install et sélectionnez "Package Control : Install Package"
    * une autre fenêtre s'ouvre, commencez à taper latex puis cherchez latextools
    * Une fenêtre s'ouvre, commencez à taper Install et sélectionnez "Package Control : Install Package"
    * une autre fenêtre s'ouvre, commencez à taper latex puis cherchez latex-cwl
  * Redémarrez Sublime Text, lorsque vous êtes sur un fichier .tex, appuyez sur f7 pour compiler. Le PDF doit normalement s'ouvrir tout seul.

## Utilisation
  * Les fichiers sources peuvent êtres compilés par le makefile
  * ou bien avec latexmk (produit des fichiers auxiliaires dans le dossier racine)
