# Webserv-explination

What is TCP/IP ?
--------------

TCP/IP stands for Transmission Control Protocol/Internet Protocol and is a suite of communication protocols used to interconnect network devices on the internet. TCP/IP is also used as a communications protocol in a private computer network (an intranet or extranet).

TCP defines how applications can create channels of communication across a network. It also manages how a message is assembled into smaller packets before they are then transmitted over the internet and reassembled in the right order at the destination address.






levels:

<img width="594" alt="Screen Shot 2023-03-13 at 11 40 29 AM" src="https://user-images.githubusercontent.com/87101785/224678598-0ee5e092-87ee-4f82-9a25-de47e4ae8cf9.png">



TCP/IP carefully defines how information moves from sender to receiver. First, application programs send messages or streams of data to one of the Internet Transport Layer Protocols, either the User Datagram Protocol (UDP) or the Transmission Control Protocol (TCP). These protocols receive the data from the application, divide it into smaller pieces called packets, add a destination address, and then pass the packets along to the next protocol layer, the Internet Network layer.

The Internet Network layer encloses the packet in an Internet Protocol (IP) datagram, puts in the datagram header and trailer, decides where to send the datagram (either directly to a destination or else to a gateway), and passes the datagram on to the Network Interface layer.

The Network Interface layer accepts IP datagrams and transmits them as frames over a specific network hardware, such as Ethernet or Token-Ring networks.

What is OSI?
-----------

The OSI reference model defines how applications can communicate over a network.

 🌱 What is HTTP?
------------

The Hypertext Transfer Protocol (HTTP) is the foundation of the World Wide Web, and is used to load webpages using hypertext links. HTTP is an application layer protocol designed to transfer information between networked devices and runs on top of other layers of the network protocol stack. A typical flow over HTTP involves a client machine making a request to a server, which then sends a response message.


C'est un protocole la plus utiliser sur internet, il pêrmet un navigateur d'obtenir des page web.

le navigateur web est une application client qui accède aux ressources stockees sur un serveur web.

Lorsque une URL est saisie au niveau des navigateur web client, le client http envoyer un requête http au serveur, le protocole http au niveau de serveur http s'éxecute en arriere plan, donc il s'agie d'un service, donc ce service il va traiter la requête http et il envois ce que n'appele une reponse http.


 🌱 La structure d'une requite HTTP:
-------------------------------





<img width="446" alt="Screen Shot 2023-03-10 at 11 55 16 AM" src="https://user-images.githubusercontent.com/87101785/224298314-ffc5c25c-f99f-45c6-a59b-156489bba8b5.png">




💬💬💬💬💬💬💬💬💬💬💬-------------------------------->Une requête http comprend 3 parties :💬💬💬💬💬💬💬💬💬💬💬💬
*******************************



📫 1 ******: une ligne de commades: 📫

-> La ligne du commande il est composer de trois partie:

🔭 Partie 1: 

La methode-> qui peux être sois de type :

👨‍💻 GET ---> demander des page HTML (La requête http il est envoyer pour demander une page html)

👨‍💻 HEAD ---> le client il est entrain de demander a travers la requête http des informations sur une ressource sans demander la ressource elle-même.

👨‍💻 POST---->  envoyer des donnéer saisies dans un formulaire integré a une page web au serveur web (Quand le client saisie ses informations dans un formulaire et ses informations il vont être envoiyer dans une requête http)

🔭 Partie 2:


URL-> Pour identifier la ressource

🔭 Partie 3:


Il dois être séparer du reste de la requête par une ligne vide. Il contient les donner a fournir au serveur(cet partie il est utiliser lorsque le client il veux envoyer des donner au serveur).



📫 2 ********: Une liste d'entêtes avec leur valeur 📫 

📫 3 ********: Le corps de la requêtes(facultatif). 📫





💬💬💬💬💬💬💬💬💬💬💬💬💬--------------------------------> Réponse HTTP:💬💬💬💬💬💬💬💬💬💬💬💬💬💬💬💬
*********************************************************************




Une reponse HTTP contient des donner envoyer depuis le serveur (Les donner recue peuvent être  de différent types(Données en text clair ou html, blug-in donnees nécessitant un autre service au programme ou .....))

Pour aider le navigateur a determiner le type de fichier qu'il recois, le serveur indique le type de donner que contient le fichier



 🌱  example:
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



<img width="1901" alt="Screen Shot 2023-03-10 at 12 36 05 PM" src="https://user-images.githubusercontent.com/87101785/224306249-8604456e-7ecd-485d-b018-cb54e7422207.png">


donc ici une requête http est envoyer au serveur consérner, aprés le serveur il va traiter la requéte et apres il va envoyer la ressouce demander (la page www.example.com/index.html)


2: Protocole:
************************


2.1: What is protocole:
----------------------

a protocol can be defined as a set of rules convensions and data structures that dictate how devices extchange data across a networks. In other words network protocols can be equated to languages that two devices most understand for seamless communication of information, regardless of their infrastructure and design desparities.

A network protocol is an established set of rules that determine how data is transmitted between different devices in the same network. Essentially, it allows connected devices to communicate with each other, regardless of any differences in their internal processes, structure or design. Network protocols are the reason you can easily communicate with people all over the world, and thus play a critical role in modern digital communications.

Similar to the way that speaking the same language simplifies communication between two people, network protocols make it possible for devices to interact with each other because of predetermined rules built into devices’ software and hardware. Neither local area networks (LAN) nor wide area networks (WAN) could function the way they do today without the use of network protocols.


Protocols are sets of rules for message formats and procedures that allow machines and application programs to exchange information. These rules must be followed by each machine involved in the communication in order for the receiving host to be able to understand the message.

2.2: List of Network Protocols:
-------------------------------

There are thousands of different network protocols, but they all perform one of three primary actions:

1-> Communication

2->Network management

3->Security


----------DNS:

Domain name system. DNS is a database that includes a website's domain name, which people use to access the website, and its corresponding IP addresses, which devices use to locate the website. DNS translates the domain name into IP addresses, and these translations are included within the DNS. Servers can cache DNS data, which is required to access the websites. DNS also includes the DNS protocol, which is within the IP suite and details the specifications DNS uses to translate and communicate.

--------DHCP:

Dynamic Host Configuration Protocol. DHCP assigns IP addresses to network endpoints so they can communicate with other network endpoints over IP. Whenever a device joins a network with a DHCP server for the first time, DHCP automatically assigns it a new IP address and continues to do so each time a device moves locations on the network.

When a device connects to a network, a DHCP handshake takes place, where the device and DHCP server communicate. The device establishes a connection; the server receives it and provides available IP addresses; the device requests an IP address; and the server confirms it to complete the process.

Every device on a TCP/IP-based network must have a unique unicast IP address to access the network and its resources. Without DHCP, IP addresses for new computers or computers that are moved from one subnet to another must be configured manually; IP addresses for computers that are removed from the network must be manually reclaimed.



---------FTP:

FTP stands for File transfer protocol.

FTP is a standard internet protocol provided by TCP/IP used for transmitting the files from one host to another.

It is mainly used for transferring the web page files from their creator to the computer that acts as a server for other computers on the internet.

It is also used for downloading the files to computer from other servers.




Objectives of FTP:

It provides the sharing of files.

It is used to encourage the use of remote computers.

It transfers the data more reliably and efficiently.



--------IP:

The Internet Protocol (IP) is a protocol, or set of rules, for routing and addressing packets of data so that they can travel across networks and arrive at the correct destination. Data traversing the Internet is divided into smaller pieces, called packets. IP information is attached to each packet, and this information helps routers to send packets to the right place. Every device or domain that connects to the Internet is assigned an IP address, and as packets are directed to the IP address attached to them, data arrives where it is needed.

Once the packets arrive at their destination, they are handled differently depending on which transport protocol is used in combination with IP. The most common transport protocols are TCP and UDP.

--------Telnet:

TELNET stands for Teletype Network. It is a type of protocol that enables one computer to connect to local computer. It used as a standard TCP/IP protocol for virtual terminal service which is provided by ISO. The computer which starts the connection is known as the local computer. The computer which is being connected to i.e. which accepts the connection known as the remote computer. During telnet operation, whatever is being performed on the remote computer will be displayed by the local computer. Telnet operates on client/server principle. The local computer uses telnet client program and the remote computers uses telnet server program. 


------TCP/UDP:

TCP et UDP se trouvent dans la quatrième couche du modèle OSI qui est la couche de transport juste au-dessus de la couche IP. TCP et UDP les deux supportent la transmission de données de deux manières différentes, TCP est en mode orienté connexion et UDP est en mode non-connecté.

TCP est un protocole fiable de bout en bout orienté connexion pour garantir la transmission de données. Certaines des principales caractéristiques de TCP sont (SYN, SYN-ACK, ACK), la détection d’erreur, le démarrage lent, le contrôle de flux et le contrôle de congestion.

UDP est un protocole de transmission simple qui fournit un service non fiable. Cela ne signifie pas que UDP ne fournira pas les données mais il n’y a pas de mécanismes pour surveiller le contrôle de congestion ou la perte de paquets, etc. Comme c’est simple, cela évite le traitement du congestion. Les applications en temps réel utilisent principalement UDP car la suppression des paquets est préférable. Un exemple typique est celui des flux de média (Streaming)

🌱 Ressources:
------------

https://www.youtube.com/watch?v=auhEJDGHI8Q

https://www.youtube.com/watch?v=2JYT5f2isg4

https://www.youtube.com/watch?v=YqEqjODUkWY&list=PLPUbh_UILtZW1spXkwszDBN9YhtB0tFKC&index=2

https://developer.mozilla.org/en-US/docs/Web/HTTP
