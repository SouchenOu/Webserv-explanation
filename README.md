# Web-serve-explination

What is HTTP?
------------

The Hypertext Transfer Protocol (HTTP) is the foundation of the World Wide Web, and is used to load webpages using hypertext links. HTTP is an application layer protocol designed to transfer information between networked devices and runs on top of other layers of the network protocol stack. A typical flow over HTTP involves a client machine making a request to a server, which then sends a response message.


C'est un protocole la plus utiliser sur internet, il pêrmet un navigateur d'obtenir des page web.

le navigateur web est une application client qui accède aux ressources stockees sur un serveur web.

Lorsque une URL est saisie au niveau des navigateur web client, le client http envoyer un requête http au serveur, le protocole http au niveau de serveur http s'éxecute en arriere plan, donc il s'agie d'un service, donc ce service il va traiter la requête http et il envois ce que n'appele une reponse http.


La structure d'une requite HTTP:
-------------------------------





<img width="446" alt="Screen Shot 2023-03-10 at 11 55 16 AM" src="https://user-images.githubusercontent.com/87101785/224298314-ffc5c25c-f99f-45c6-a59b-156489bba8b5.png">




-------------------------------->Une requête http comprend 3 parties :

1 ******: une ligne de commades:

-> La ligne du commande il est composer de trois partie:

Partie 1: 
*********

La methode-> qui peux être sois de type :

GET ---> demander des page HTML (La requête http il est envoyer pour demander une page html)

HEAD ---> le client il est entrain de demander a travers la requête http des informations sur une ressource sans demander la ressource elle-même.

POST---->  envoyer des donnéer saisies dans un formulaire integré a une page web au serveur web (Quand le client saisie ses informations dans un formulaire et ses informations il vont être envoiyer dans une requête http)

Partie 2:
********

URL-> Pour identifier la ressource

Partie 3:
********

Il dois être séparer du reste de la requête par une ligne vide. Il contient les donner a fournir au serveur(cet partie il est utiliser lorsque le client il veux envoyer des donner au serveur).



2 ********: Une liste d'entêtes avec leur valeur

3 ********: Le corps de la requêtes(facultatif).

--------------------------------> Réponse HTTP:

Une reponse HTTP contient des donner envoyer depuis le serveur (Les donner recue peuvent être  de différent types(Données en text clair ou html, blug-in donnees nécessitant un autre service au programme ou .....))

Pour aider le navigateur a determiner le type de fichier qu'il recois, le serveur indique le type de donner que contient le fichier



Un example:
------------


<img width="810" alt="Screen Shot 2023-03-10 at 12 22 38 PM" src="https://user-images.githubusercontent.com/87101785/224303727-09e580df-3f57-45f8-bd55-3676f36524a7.png">

l'utilisateur saisie URL suivant : http://www.example.com

les etapes:

1: Le navigateur interprète les trois partie de L'URL(Uniform ressorce locator):

il saura que :

*Le protocol--> HTTP

*Le nom du domaine --> www.example.com

*resource demainder --> c'est la page index.html

2: a partir du prefix http du URL, le navigateur determine que le protocole a utiliser est http, ainsi il definie 80 comme numéro de port destination et un numéro aléatoire comme numéro de port source. 

3: cash DNS qui est consulter pour extraire l'address IP qui correspont le nom du domaine


<img width="810" alt="Screen Shot 2023-03-10 at 12 35 30 PM" src="https://user-images.githubusercontent.com/87101785/224306139-0d91bce5-e36a-4b9d-9d97-2bae5ced5c09.png">


<img width="1901" alt="Screen Shot 2023-03-10 at 12 36 05 PM" src="https://user-images.githubusercontent.com/87101785/224306249-8604456e-7ecd-485d-b018-cb54e7422207.png">


donc ici une requête http est envoyer au serveur consérner, aprés le serveur il va traiter la requéte et apres il va envoyer la ressouce demander (la page www.example.com/index.html)








Ressources:
------------

https://www.youtube.com/watch?v=auhEJDGHI8Q

https://www.youtube.com/watch?v=2JYT5f2isg4

https://www.youtube.com/watch?v=YqEqjODUkWY&list=PLPUbh_UILtZW1spXkwszDBN9YhtB0tFKC&index=2
