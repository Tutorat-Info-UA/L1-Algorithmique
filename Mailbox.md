# ✉️ Mailbox
Cet exercice vous permettra de vous exercer sur différentes notion :
 - Chaîne de caractère 
 - Fonction
 - Tableau
 - Structure
 - Boucle for et while
 - Iostream


Nous souhaitons créer un système de sauvegarde de brouillon pour une boîte mail.

# Exercice 1
- Créer votre structure de données mail box qui permet de sauvegarder un ensemble de chaîne de caratère, le mieux et d'utiliser une structure.
- Créer une procèdure qui permet de remplir votre tableau
- Dans main créer une boucle while qui permet de remplir votre tableau jusqu'a que la commande `/stop` soit indiqué dans le terminal
- Créer une procédure qui permet d'afficher tout le tableau 
- Dans main ajouté une commande `/showall` qui permet d'afficher tout les messages

Voici un exemple de déroulement :
```
<< /msg Salut vais bien.
<< /msg Il fait beau aujourd'hui.
<< /show all 

--- Brouillon enregistrée ---

0: Salut je vais bien.
1: Il fait beau aujourd'hui.

<< /msg Je vais au super marché
<< /stop
```

# Exercice 2
- Créer une fonction `bool is_substring(std::string s, std::string ss)` qui retourne vrais si `ss` est sous chaine de `s`
- Créer une fonction `int shearch_first(Mailbox m, std::string ss)` qui retourne le premier indice du message qui contient la sous chaine `ss`
- Ajouté la commande `/shearch_first {ss}` à votre programme principal  qui retourne le premier message correspondant

Voici un exemple de déroulement :

```
<< /msg Salut vais bien.
<< /msg Il fait beau aujourd'hui.
<< /shearch_first Salut

--- Brouillon enregistrée pour la recherche "Salut" ---
0: Salut je vais bien.

<</stop
```

