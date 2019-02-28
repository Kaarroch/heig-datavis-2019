Il faut définir une hauteur et une largeur au contexte SVG, c'est-à-dire la zone ou tous les éléments visuels seront visibles
Ce contexte se définit par width = x, height = y.
Ensuite, il faut avoir des données concernant un sujet. On peut créer des tableaux pour ranger des données.
Par exemple, on a créé un tableau 'fruits' pour ranger les informations concernant le nom et la quantité de chaque fruit
que nous voulons représenter graphiquement. fruits = ([{name: 'Pomme', num: 5}, {name: 'Pêche', num: 3 }, { name: 'Banane', num: 6 }])
Si nous voulons représenter les bâtons en hauteur, on peut définir une largeur fixe pour tous les bâtons, comme LARGEUR_BATON = 50.
la fonction fruits.map permet de lister tous les fruits. On crée un nombre de bâtons = au nombre de fruits dans le tableau.
Si x = largeur totale des bâtons, alors x = index*LARGEUR_BATON.
La hauteur de chaque bâton = quantité de chaque fruit respectif. Pour calculer cette hauteur, il suffit de faire la taille totale du
contexte SVG - quantité de chaque fruit. La hauteur de chaque bâton se calcul automatiquement selon un poucentage. Si la quantité maximum d'un fruit est de 6, alors 6 vaudra 100% de la hauteur du contexte, et si la quantité d'un fruit est de 3, alors la hauteur du bâton de ce fruit sera 50% de la hauteur du contexte.