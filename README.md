## MarkDown pour SPIP (experimental)

Ce plugin permet d'utiliser la syntaxe markdown dans un article SPIP.
Le texte � interpr�ter en markdown doit �tre entre `<md>...</md>`

Les corrections typographiques de SPIP (li�es � la langue) sont appliqu�es dans le MarkDown.

Les raccourcis de liens SPIP et les mod�les sont interpr�t�s dans le markdown,
ce qui permet d'�crire des liens indiff�rement avec la syntaxe SPIP ou la syntaxe markdown


### Tests unitaires

Le plugin repose sur la librairie http://parsedown.org/ dont il reprend les tests unitaires qui sont tous valides
dans un raccourci `<md>..</md>`, ce qui garanti qu'on ne perturbe pas la syntaxe MarkDown par la prise en charge
de la typographie ainsi que des raccourcis de lien SPIP (Tests `parsedown`).

Un jeu de tests compl�mentaire concerne aussi le respect de la syntaxe markdown, mais porte sur des cas limites
g�n�r�s par l'interaction entre le moteur SPIP et le moteur Parsedown (Tests `markdown`).

Un jeu de tests unitaires assure que le corrections typographiques sont bien appliqu�es l� et uniquement l�
o� c'est attendu dans le texte au format MarkDown (Tests `markdown_typo`).

Un jeu de tests unitaires concerne la prise en charge des raccourcis de liens SPIP dans le MarkDown (Tests `markdown_liens_spip`).

Un jeu de tests unitaires reste � �crire sur la prise en charge des mod�les SPIP dans le texte MarkDown.

### TODO
Proposer un formulaire de configuration qui permette de choisir le fonctionnement du plugin :
- Appliquer la syntaxe SPIP par d�faut et la syntaxe MarkDown dans les blocs `<md>..</md>`
- Appliquer la syntaxe MarkDown par d�faut et la syntaxe SPIP dans les blocs `<spip>..</spip>`
  Cette derni�re configuration est particuli�rement int�ressante dans le cadre d'un nouveau site
  mais n�cessiterait une migration des contenus d'un site existant.