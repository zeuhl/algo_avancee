########################################################################
#																	   #
#						Info 724 - Projet de TP                        #
#						 										       #
#							M1 - STIC - Info                           #
#							       									   #
#							  2014 / 2015							   #
#							  										   #
#					  Caillet / Burnet / Mollard			           #
#							  										   #
########################################################################

Explication du fonctionnement des 3 éxecutables :

########################################################################
########################################################################

-- Pré-utilisation :

Les 3 executable sont disponible dans le dossier "src" présent à la
racine de l'archive.
	
	- Le réducteur    : ./src/P1_3COL_Reducteur.py
	- Le solveur      : ./src/P1_3COL_Solveur.py
	- Le vérificateur : ./src/P1_3COL_Verificateur.py
	
A verifier avant les manipulations :

	- Verifier que les fichiers soient bien executable. (ls -l)
			--> Si pas executable faire  : "sudo chmod +x ../src/P1*" 

	- Verifier la présence du compilateur Python2.7 sur votre machine
			--> "python --version"

########################################################################
########################################################################

-- Utilisation : 

Reducteur : ( ./src/P1_3COL_Reducteur.py )

Le reducteur prend en entrée une instance du probléme P2 (3SAT).

	- Deux solutions pour tester : (Dans un terminal)
	
	1 ) Passer la commande suivante :
	
	cat "instance_de_P2" | ./src/./P1_3COL_Reducteur 
	
	2 ) 
	
	cat "intance_de_P2" | python2.7 ./src/P1_3COL_Reducteur.py
	
	- Pour verifier faire :
	
	echo $?
	
		--> Si 0 : OK
		--> Si 1 : NOK
		
########################################################################

Solveur : ( ./src/P1_3COL_Solveur.py )
	
Le solveur prend en entrée un graph au format suivant :

Graph {
1 2 3 4 //Liste sommets
1--2
2--3    //Les arrêtes du graph
...
}	
	
	- Deux solution pour tester : (Dans un terminal)
	
	1 ) Passer la commande suivante :
	
	cat "graph" | ./src/./P1_3COL_Solveur
	
	2 ) 
	
	cat "graph" | python2.7 ./src/P1_3COL_Solveur.py
	
	- Pour verifier faire :
	
	echo $?
	
		--> Si 0 : OK
		--> Si 1 : NOK 

########################################################################

Verificateur : ( ./src/P1_3COL_Verificateur.py )

Le verificateur prend en entrée un graph et un certificat.

Format du graph :

Graph {
1 2 3 4 //Liste sommets
1--2
2--3    //Les arrêtes du graph
...
}

Format du certificat :

Colors {
c--1--"jaune" //Le "c" signifie couleur
c--2--"rouge" //"c--numero_sommet--couleur_associée"
c--3--"vert"
c--4--"jaune"
}

L'ordre des arguments d'entrée est importante , il faut en premier
donner le graph puis en second le certificat.

	- Deux solution pour tester : (Dans un terminal)
	
	1 ) Passer la commande suivante :
	
	cat "graph" "certificat" | ./src/./P1_3COL_Verificateur


	2 ) 
	
	cat "graph" "certificat" | python2.7 ./src/P1_3COL_Verificateur.py
	
	- Pour verifier faire :
	
	echo $?
	
		--> Si 0 : OK
		--> Si 1 : NO
	
