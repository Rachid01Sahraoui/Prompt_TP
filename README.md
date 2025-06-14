# Prompt_TP
TP : Ingénierie de prompt appliquée à la 
génération de code avec l’IA 



1. Solution choisie :
Blackbox AI



2. Définition brève de la solution :
Blackbox AI est une plateforme d’IA générative spécialisée dans la génération et l'autocomplétion de code source à partir de prompts en langage naturel. Elle prend en charge plusieurs langages de programmation et peut être intégrée dans des environnements de développement comme VS Code ou utilisée via son interface web.



3. Avantages perçus de cette solution pour le développement de code :
✅ Support multilingue : Blackbox AI prend en charge plus de 20 langages de programmation, ce qui la rend très polyvalente.

✅ Extraction de code à partir de vidéos et de captures d’écran : elle permet de copier du code directement depuis des tutoriels vidéo ou des images, ce qui peut accélérer l’apprentissage et la reproduction de solutions.

✅ Interface simple et rapide : la plateforme est accessible et réactive, idéale pour des générations rapides sans configuration complexe.



4. Inconvénients ou limites perçues de cette solution :
⚠️ Compréhension contextuelle limitée : par rapport à des IA comme ChatGPT, Blackbox AI peut parfois manquer de finesse dans la compréhension du contexte du prompt.

⚠️ Peu de personnalisation du style de code généré : les résultats peuvent varier en qualité et en structure.

⚠️ Moins adaptée au débogage ou à l’explication détaillée du code : elle est performante pour générer du code, mais moins utile pour des tâches pédagogiques ou de refactoring avancé.



5. Cas d'utilisation typiques :
🔹 Génération rapide de fonctions simples à partir de descriptions naturelles.

🔹 Autocomplétion dans un IDE pour accélérer le codage.

🔹 Extraction de code depuis des sources non textuelles (vidéos YouTube, captures d’écran).

🔹 Prototypage rapide ou génération de snippets pour tester des idées.



 Conclusion sur le prompt vague :
Le code fonctionne pour les cas de base.

La compréhension de la tâche est correcte, mais limitée.

Manque de robustesse, de style professionnel, et de bonnes pratiques Python.

Le vocabulaire utilisé (addition, etc.) dépend fortement de la langue du prompt, ce qui peut limiter la réutilisabilité.




  L'analyse comparative entre la version générée avec le prompt vague et celle avec le prompt spécifique :
✅ 1. Robustesse
Critère	Prompt vague (operations)	Prompt spécifique (calculate)
Gestion division par zéro	Oui (retourne message)	Oui (retourne message)
Opérations invalides	Oui, mais message générique	Oui, avec message clair
Validation des entrées	Non	Non (mais pas demandée dans le prompt)
Arrondi pour division	❌ Non arrondi	✅ Résultat arrondi à deux décimales

✔️ Conclusion : La version spécifique est plus robuste, car elle gère mieux la division et donne des messages clairs.

🧾 2. Lisibilité
Élément	Prompt vague	Prompt spécifique
Noms de fonction/paramètres	operations(a, b, operation)	calculate(a, b, op) ✔️ court et clair
Langue des opérations	Français ('addition') ❌	Symboles mathématiques ('+', etc.) ✔️
Commentaires	❌ Aucun	✅ Docstring bien structuré
Structure du code	Basique	Structurée et lisible

✔️ Conclusion : Le code issu du prompt spécifique est nettement plus lisible et plus professionnel.

🔁 3. Couverture des cas
Cas	Prompt vague	Prompt spécifique
calculate(10, 5, '+')	Oui	Oui
Division par zéro	Oui	Oui
Opération invalide (%)	Oui	Oui
Arrondi sur division	❌ Non	✅ Oui
Utilisation d'autres langues (add)	❌ Oui, mais inadapté	✅ Adapté aux conventions courantes

✔️ Conclusion : Le prompt spécifique couvre mieux les cas attendus et suit des conventions plus universelles.

🧠 Résumé de la comparaison
Critère	Vague	Spécifique
Robustesse	🟡 Moyenne	🟢 Élevée
Lisibilité	🔴 Faible	🟢 Très bonne
Bonne pratique	🔴 Non respectées	🟢 Respectées
Clarté du code	🟡 Moyenne	🟢 Très claire
Gestion des erreurs	🟡 Basique	🟢 Complète




  La version générée avec un prompt avec persona est clairement plus professionnelle, mieux structurée, et plus sécurisée. Voici une évaluation détaillée :

✅ 1. Le code est-il plus professionnel ?
Oui. Plusieurs éléments montrent une amélioration significative :

✅ Utilisation d’un docstring clair et structuré au format conventionnel.

✅ Respect des conventions PEP8 (indentation, espacement, noms explicites).

✅ Ajout du bloc if __name__ == "__main__": → bonne pratique Python.

✅ Des commentaires pertinents accompagnent les sections critiques.

🧱 2. Le code est-il mieux structuré ?
Oui. Par rapport aux versions précédentes :

La logique est simple et linéaire.

Les conditions sont clairement séparées.

Chaque branche (if, elif, else) couvre un cas spécifique identifiable.

Il y a une séparation nette entre la définition de la fonction et son utilisation/test.

🔐 3. Le code est-il plus sécurisé ?
Oui, relativement :

✔️ Division par zéro bien gérée avec une condition if b == 0.

✔️ Opérateurs non valides détectés et renvoient un message d’erreur.

❗ Limite : Le code retourne des chaînes d'erreur ("Erreur : ..."), ce qui pourrait poser problème dans un contexte d’intégration (où l’on préférerait lever une exception pour une meilleure gestion de flux d’exécution).



📊 Résumé comparatif global :
Critère	Prompt vague	Prompt spécifique	Prompt avec persona
Nom explicite	🟡 Moyen	✅ Oui	✅ Oui
Docstring	❌ Non	✅ Basique	✅ Complet
Gestion erreurs	🟡 Partielle	✅ Bonne	✅ Très bonne
Respect PEP8	❌ Non	🟡 Approximatif	✅ Oui
Commentaires	❌ Aucun	✅ Minimes	✅ Pertinents
Séparation exécution/test	❌ Non	❌ Non	✅ Présente


🧠 Conclusion :
✅ Le prompt avec persona produit un code :

plus clair,

plus maintenable,

plus conforme aux bonnes pratiques professionnelles.



Analyse Critique : 

1)  Le prompt vague produit du code basique et incomplet.

Le prompt spécifique améliore nettement la qualité, la clarté et la robustesse.

Le prompt avec persona donne un résultat quasi professionnel, montrant que la formulation du prompt influence directement la qualité du code généré.


2)  Le principe de “persona” a eu l’impact le plus significatif, car il oriente l’IA vers une production de code conforme aux standards professionnels, à la fois sur le fond et sur la forme.


3)  Oui, l’IA a introduit des erreurs ou comportements inattendus dans certaines versions, surtout lorsqu’elle était guidée par un prompt vague ou insuffisamment précis.

 Erreurs dans la version générée avec le prompt vague :
Langue des opérateurs : L’IA a utilisé des noms d’opérations en français ('addition', 'soustraction'), ce qui n’était pas attendu si l’on s’attendait à des symboles ('+', '-'). Cela limite la réutilisabilité du code.

Gestion des erreurs rudimentaire : Au lieu de lever des exceptions (raise), l’IA a simplement retourné des chaînes de caractères comme "Erreur : Division par zéro". Cela peut créer des incohérences si l’on attend un résultat numérique.

Absence de contrôle sur les types d’entrée : Aucun mécanisme ne vérifie si a et b sont bien des entiers, ce qui pourrait provoquer des erreurs à l’exécution si des types inattendus sont passés.

Ces erreurs montrent que la qualité et la précision du prompt sont cruciales pour éviter des comportements inattendus de l’IA. Le passage à un prompt spécifique ou avec persona permet de fortement limiter ces problèmes.


4)  Utiliser un prompt vague pour générer du code avec l’IA entraîne un coût plus élevé en temps et en effort, car le code produit est souvent incomplet, peu structuré et nécessite de nombreuses corrections manuelles (15 à 30 minutes de travail). À l’inverse, un prompt spécifique permet d’obtenir un code plus clair, plus robuste et plus proche des standards professionnels, avec peu ou pas de modifications nécessaires (5 à 10 minutes). En résumé, un prompt bien formulé réduit considérablement le travail humain en guidant mieux l’IA, rendant le processus plus efficace et le résultat plus fiable.



Exercice 2.2 : 



le code généré est correct et robuste face aux erreurs. Il respecte les contraintes du prompt en vérifiant que l’identifiant est bien une chaîne de 10 caractères alphanumériques et en levant une ValueError en cas de non-conformité. La structure est claire, les messages d’erreur sont explicites, et les tests d’exécution couvrent les cas valides et invalides. La fonction est donc fiable et bien conçue pour un usage standard.



L’ajout d’un exemple concret dans le prompt a clairement simplifié la tâche de l’IA et amélioré la qualité du code généré. Par rapport au résultat précédent, où les tirets étaient placés après le 3ᵉ et le 7ᵉ caractère (selon une interprétation textuelle du prompt), cette version place les tirets au bon endroit (après le 3ᵉ et le 6ᵉ caractère), comme indiqué par l’exemple d’entrée-sortie fourni.

L’exemple a donc éliminé toute ambiguïté, en guidant l’IA vers le format attendu, ce qui a permis :

Une meilleure compréhension de la logique de découpage de la chaîne.

L’éviction d’erreurs de placement de tirets.

Une génération de code plus précise et fidèle à l’intention du prompt.

En résumé, oui, l’exemple a été très utile pour orienter l’IA et a contribué à un code plus correct et aligné avec les attentes fonctionnelles.





Oui, l’ajout du deuxième exemple valide et surtout du cas d’erreur explicite dans le prompt a permis à l’IA de mieux anticiper et gérer les erreurs. Grâce à ces exemples concrets, la fonction générée est plus robuste et répond exactement aux attentes. En particulier :

✅ Le contrôle de la longueur de la chaîne fonctionne bien.

✅ La vérification des caractères alphanumériques est présente.

✅ Les messages d’erreur sont clairs et informatifs.

✅ Les tests incluent à la fois des cas valides et un cas invalide, ce qui renforce la fiabilité du code.

En résumé, la robustesse du code a été améliorée grâce à une meilleure formulation du prompt et à l’ajout d’exemples précis. Cela montre à quel point les exemples d’entrée-sortie guident efficacement l’IA pour produire un code de qualité, complet et sûr.


Analyse Critique: 

Influence des exemples sur la compréhension de l’IA :
L’ajout d’exemples concrets dans le prompt améliore significativement la capacité de l’IA à interpréter correctement les consignes, notamment lorsqu’elles comportent des règles complexes ou implicites. Dans le cas de la fonction format_product_code, les exemples d’entrée-sortie ont supprimé toute ambiguïté sur l’emplacement des tirets, ce qui aurait pu être mal interprété par une simple description textuelle. De plus, en intégrant un cas d’erreur explicite (par exemple une chaîne trop courte), l’IA a pu mieux modéliser le comportement attendu en cas d’entrée invalide. Ainsi, les exemples servent à ancrer les règles de manière opérationnelle et à guider la génération d’un code plus précis, robuste et conforme.

Utilité du Few-Shot Prompting en développement :
Le "Few-Shot Prompting" est particulièrement utile en développement lorsqu’on cherche à générer du code qui suit des règles spécifiques, des formats bien définis, ou qui doit gérer des cas limites et erreurs de manière fiable. Il est aussi très pertinent pour montrer des patterns réutilisables, comme des boucles ou des structures conditionnelles, sans avoir à expliquer la logique sous-jacente dans le prompt. Dans le contexte d’outils génératifs, cela permet de réduire les malentendus entre la formulation naturelle du prompt et l’implémentation attendue, tout en accélérant la production de code conforme à des standards ou à des cas d’usage concrets.

Limites liées aux exemples fournis :
Bien que les exemples soient très puissants, ils ont leurs limites. D’abord, trop d’exemples peuvent allonger inutilement le prompt et dépasser les limites de contexte du modèle, ce qui peut altérer les performances. Ensuite, la qualité des exemples est cruciale : des exemples erronés ou ambigus peuvent induire l’IA en erreur. Enfin, les exemples ne remplacent pas toujours une bonne description : si les cas ne couvrent pas suffisamment de scénarios (erreurs inattendues, types de données différents, etc.), le code généré pourrait rester incomplet. Il est donc essentiel de trouver un équilibre entre quantité, diversité et pertinence des exemples pour tirer pleinement parti du Few-Shot Prompting.



Exercice 2.3 : 



Prompt vague :
Crée une mini-application Web qui fonctionne comme une calculatrice simple avec HTML, CSS et JavaScript.




 Prompt détaillé (spécifique) :
Génère une mini-application Web (une seule page) qui simule une calculatrice simple avec HTML, CSS et JavaScript pur (sans frameworks).

Fonctionnalités attendues :

Opérations de base : addition, soustraction, multiplication, division.

Interface avec une zone d’affichage en haut, suivie d’une grille de boutons (0 à 9, +, −, ×, ÷, =, C).

Bouton “C” pour effacer l’entrée actuelle.

Prise en charge des erreurs comme la division par zéro (afficher “Erreur” dans l’écran).

Exigences visuelles :

Design simple mais responsive (adapté aux petits écrans).

Boutons de forme carrée avec un effet de survol (hover).

Affichage avec fond sombre et chiffres en clair.

JavaScript :

Utilise un seul fichier JS pour gérer les interactions.

Aucune bibliothèque externe.

Le calcul doit être géré proprement (sans eval()).


Avec le prompt vague, l’IA a généré une calculatrice simple, mais elle a dû faire des suppositions :

Le design est correct mais basique.

La logique est minimaliste : chaque bouton agit indépendamment, les opérations sont linéaires.

Aucune gestion fine des erreurs ou des cas limites (ex : double opérateur, nombre à virgule, saisie clavier).

En revanche, le prompt détaillé a permis à l’IA :

de comprendre précisément le comportement attendu (comme remplacer un opérateur si on en entre deux à la suite),

de prendre en compte des contraintes de langue (gestion de la virgule française ,),

d’ajouter une vraie robustesse avec try...catch, Function, gestion du clavier, aria-live, etc.

 Conclusion : plus le prompt est détaillé (exemples + règles spécifiques), plus l’IA peut structurer du code robuste, lisible et proche des attentes réelles.



Execrice 3.1 : Débogage assisté

1)  Résultat à l’exécution :   
Traceback (most recent call last):
  File "main.py", line 11, in <module>
    avg = calculate_average(my_nums)
  File "main.py", line 6, in calculate_average
    total += num
TypeError: unsupported operand type(s) for +=: 'int' and 'str'

2) Je travaille sur une fonction Python nommée calculate_average qui doit calculer la moyenne d’une liste de nombres. Voici le code que j’ai utilisé :
def calculate_average(numbers_list):
# This function calculates the average of numbers in a list
# It has some issues
total = 0
for num in numbers_list:
total += num
average = total / len(numbers_list)
return average

#Example of usage (might cause errors)
my_nums = [1, 2, 'three', 4]
avg = calculate_average(my_nums)
print(f"Average: {avg}")
Lorsque j'exécute ce code, j'obtiens l'erreur suivante :
Traceback (most recent call last):
File "main.py", line 11, in <module>
avg = calculate_average(my_nums)
File "main.py", line 6, in calculate_average
total += num
TypeError: unsupported operand type(s) for +=: 'int' and 'str'
Peux-tu :
Identifier clairement la cause de cette erreur ?
Proposer une correction du code pour qu’il fonctionne avec une liste contenant éventuellement des valeurs non numériques ?
Merci !


3)  Peux-tu générer une suite de tests unitaires en utilisant pytest pour valider le comportement de la fonction calculate_average(numbers_list) ?

Les tests doivent vérifier notamment :

le calcul correct avec une liste de nombres (entiers et flottants),

le comportement avec une liste contenant des valeurs non numériques (doivent être ignorées ou provoquer une erreur selon ta correction),

la gestion d’une liste vide,

la gestion d’une liste contenant uniquement des éléments non numériques.

Execrice 3.2 : Refactoring avec l’IA

1) Le code fourni a pour fonction de trier une liste d’entiers en ordre croissant en utilisant un algorithme de tri simple, semblable au tri par sélection. Il compare chaque élément de la liste à tous ceux qui le suivent, et échange les valeurs si nécessaire. Toutefois, ce code présente plusieurs défauts importants de lisibilité et de structure. Premièrement, les noms des variables sont peu explicites : par exemple, a ne dit rien sur le contenu (une liste d’entiers), et tmp n’est pas commenté ni justifié. Deuxièmement, le code est écrit sans aucune fonction, ce qui nuit à la modularité et à la réutilisabilité. Enfin, aucun commentaire n’est présent, ce qui rend difficile la compréhension de la logique, surtout pour quelqu’un qui découvre le code. Un bon refactoring consisterait à utiliser des noms significatifs, à encapsuler le tri dans une fonction, à ajouter des commentaires explicatifs, et éventuellement à remplacer ce tri naïf par une méthode plus efficace (comme sorted() en Python ou un algorithme optimisé).

2)Le code suivant trie une liste d'entiers en ordre croissant, mais il est peu lisible et non structuré. Refactore-le en suivant les bonnes pratiques de programmation :

Utilise des noms de variables explicites (par exemple numbers au lieu de a).

Crée une fonction dédiée au tri, par exemple sort_numbers(numbers: list) -> list.

Ajoute des commentaires clairs pour expliquer les étapes du tri.

Assure-toi que le code soit facile à lire et à comprendre.

Optionnel : tu peux utiliser un algorithme de tri standard si pertinent.

Voici le code de départ :
a = [5, 3, 8, 6, 7, 2] 
for i in range(len(a)): 
    for j in range(i+1, len(a)): 
        if a[i] > a[j]: 
            tmp = a[i] 
            a[i] = a[j] 
            a[j] = tmp 
print(a)

3)Le code ci-dessous trie une liste d'entiers en ordre croissant, mais il est mal structuré et difficile à lire. Refactore ce code en suivant les exigences suivantes :

Contraintes de refactoring :
Respecter la convention PEP8 (indentation, nommage, espaces, longueurs de ligne, etc.).

Utiliser des noms explicites pour toutes les variables et fonctions.

Séparer le code en fonctions modulaires, chacune ayant une seule responsabilité claire.

Ajouter des commentaires et des docstrings à chaque fonction pour expliquer son rôle, ses paramètres et sa valeur de retour.

Ajouter un bloc d’exécution conditionnel : if __name__ == "__main__": ...
Code à refactorer :
a = [5, 3, 8, 6, 7, 2] 
for i in range(len(a)): 
    for j in range(i+1, len(a)): 
        if a[i] > a[j]: 
            tmp = a[i] 
            a[i] = a[j] 
            a[j] = tmp 
print(a)

Execrice 3.3 : Génération de Documentation  

1)  j’ai une fonction Python appelée get_user_permissions qui fonctionne correctement, mais elle manque de documentation claire. Peux-tu générer un docstring complet et standardisé pour cette fonction ?
La docstring doit inclure :
une description du but de la fonction,
une description des paramètres user_id et system_context,
une description de la valeur de retour,
et un exemple d’utilisation clair.
Voici la fonction en question :
def get_user_permissions(user_id, system_context): 
    # This function fetches user permissions 
    # Needs better documentation 
    if user_id in system_context['admins']: 
        return ['read', 'write', 'delete', 'admin'] 
    elif user_id in system_context['editors']: 
        return ['read', 'write'] 
    else: 
        return ['read']


2)  j’aimerais ajouter une section à mon fichier README.md qui explique comment utiliser la fonction get_user_permissions.
Peux-tu générer une section en Markdown incluant :
une explication claire de la fonction,
les prérequis (notamment le format de system_context),
des exemples d’appel bien présentés pour différents cas d’utilisation ?
Merci !


3)  je trouve que le docstring ainsi que la section du README sont très clairs, complets et faciles à comprendre. Le docstring suit un standard structuré, explique bien le rôle de la fonction, les paramètres attendus et les valeurs retournées, tout en fournissant des exemples concrets — ce qui facilite grandement la compréhension directement depuis l'éditeur de code. Quant à la section Markdown dans le README, elle va encore plus loin en détaillant les prérequis, en illustrant plusieurs cas d'utilisation (admin, éditeur, invité) et en proposant un résumé final des permissions retournées. Cela rend l'intégration de cette fonction dans un autre projet très intuitive. En résumé, pour un autre développeur qui n’a jamais vu ce code, la documentation fournie est suffisante pour comprendre rapidement le comportement de la fonction et l’utiliser correctement sans ambiguïté.





lien vers la conversation avec Blackbox AI: 
https://www.blackbox.ai/share/2a5d2632-7a15-4a10-97e8-672a3865c0fa


