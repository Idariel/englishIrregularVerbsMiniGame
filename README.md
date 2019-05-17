# englishIrregularVerbsMiniGame
Originally named : englishVerbsMastermind

But : 
Permettre à l'utilisateur de l'application d'apprendre les verbes irréguliers en s'amusant.
Le principe a été testé,sur un bout de papier, par mon neveu de 12 ans, alors que je lui faisait réviser ses leçons. En deux secondes, nous sommes passé du "Euhhhhh" de la mort qui tue a une participation active, voir même enthousiaste du marsupilami. Quelques mois après, il se souvenait encore de la trentaine de verbes que nous avons vus ce soir-là.

A faire :
Lister les verbes défectifs anglais quelque part (array ou bdd).
Joueur dans bdd (voir mcd et mpd)

Principe du jeu :
L'application propose au joueur le verbe en français à l'infinitif.
Le joueur doit répondre en donnant l'infinitif anglais (to xxxx).

Module original : PRETERIT
Si l'infinitif n'est pas correct : BIIIPPPPPP!!!!!! (bruitage et anim sympa), le joueur doit proposer un autre infinitif ("Euhh, tu rejoues ?).

Si l'infinitif est bon, l'application lui demande le prétérit.
Réponse de l'application :
L'application répond en donnant 3 informations : 
-le nombre de lettre bien placées, 
-le nombre de lettre présentes dans le mot mais mal placées,
-une valeur X ou O (booléen) pour indiquer si le nombre de lettres du verbe au prétérit est bon (certains verbes changes d'écriture entre l'infinitf et le prétérit).

Module secondaire : PARTICIPE PASSE
Même chose avec le participe passé.


## Base de données ou array
### Array
*Pro*
- Javascript
- simple à utiliser
- uniquement en front

*Con*
- pas de données extensives

### Base de données (MongoDB ou SQL)
*Pro*
- quantité de données importante
- données croisée faciles à retrouver grâce aux tables (ou équivalent)

*Con*
- connaître le back-end et les appels à la bdd

### Début de codage de la BDD avec MongoDB
Dans le Terminal
Start the database
  *sudo service mongod start*

Access MongoDB en utilisant le shell
  *mongo --host localhost:27017*

Créer la base de données
  *use IrregularVerbEnglish*

Ajouter une collection (équivalent des tables en SQL)
  *db.createCollection("user")*
  *db.createCollection("declinaisons")*

Ajouter des données
  *db.user.insert({"firstName":"Isabelle", "familyName":"LECHAT"})*
  *db.declinaison({"verbFR":"commencer","infinitifEng":"begin","preteritEng":"began","pluperfectEng":"begun"})
