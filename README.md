# Webserv-explination


1: Web server
-------------

1.1-What is web server?
-----------------------

The term web server can refer to hardware or software, or both of them working together.

1:On the hardware side, a web server is a computer that stores web server software and a website's component files (for example, HTML documents, images, CSS stylesheets, and JavaScript files). A web server connects to the Internet and supports physical data interchange with other devices connected to the web.

2:On the software side, a web server includes several parts that control how web users access hosted files. At a minimum, this is an HTTP server. An HTTP server is software that understands URLs (web addresses) and HTTP (the protocol your browser uses to view webpages). An HTTP server can be accessed through the domain names of the websites it stores, and it delivers the content of these hosted websites to the end user's device.



At the most basic level, whenever a browser needs a file that is hosted on a web server, the browser requests the file via HTTP. When the request reaches the correct (hardware) web server, the (software) HTTP server accepts the request, finds the requested document, and sends it back to the browser, also through HTTP. (If the server doesn't find the requested document, it returns a 404 response instead.)


<img width="663" alt="Screen Shot 2023-03-13 at 4 19 39 PM" src="https://user-images.githubusercontent.com/87101785/224746231-34b20423-0930-4f2f-82d8-663201bbcb06.png">


A static web server, or stack, consists of a computer (hardware) with an HTTP server (software). We call it "static" because the server sends its hosted files as-is to your browser.

A dynamic web server consists of a static web server plus extra software, most commonly an application server and a database. We call it "dynamic" because the application server updates the hosted files before sending content to your browser via the HTTP server.


---->Deeper dive

To review: to fetch a webpage, your browser sends a request to the web server, which searches for the requested file in its own storage space. Upon finding the file, the server reads it, processes it as needed, and sends it to the browser. Let's look at those steps in more detail.

1...Hosting files

First, a web server has to store the website's files, namely all HTML documents and their related assets, including images, CSS stylesheets, JavaScript files, fonts, and video.

Technically, you could host all those files on your own computer, but it's far more convenient to store files all on a dedicated web server because:

A dedicated web server is typically more available (up and running).
Excluding downtime and system troubles, a dedicated web server is always connected to the Internet.
A dedicated web server can have the same IP address all the time. This is known as a dedicated IP address. (Not all ISPs provide a fixed IP address for home lines.)
A dedicated web server is typically maintained by a third party.

1.2-Examples of web server software
---------------------------------------



Below are examples of web server software.

Apache Web Server: official Apache website.

Nginx: official Nginx website.

Boa Webserver: official Boa website.

FoxServ Web Server: official FoxServ website.

Lighttpd: official lighttpd website.

Microsoft's Web Server, IIS: official IIS website.

Savant: official Savant website.

Tomcat: official Tomcat website.



What is TCP/IP ?
--------------

Une suite de protocoles (organisée en couche) utilisés pour le transfert des données sur internet.

......En progress

TCP/IP stands for Transmission Control Protocol/Internet Protocol and is a suite of communication protocols used to interconnect network devices on the internet. TCP/IP is also used as a communications protocol in a private computer network (an intranet or extranet).

TCP defines how applications can create channels of communication across a network. It also manages how a message is assembled into smaller packets before they are then transmitted over the internet and reassembled in the right order at the destination address.






levels:

<img width="594" alt="Screen Shot 2023-03-13 at 11 40 29 AM" src="https://user-images.githubusercontent.com/87101785/224678598-0ee5e092-87ee-4f82-9a25-de47e4ae8cf9.png">



TCP/IP carefully defines how information moves from sender to receiver. First, application programs send messages or streams of data to one of the Internet Transport Layer Protocols, either the User Datagram Protocol (UDP) or the Transmission Control Protocol (TCP). These protocols receive the data from the application, divide it into smaller pieces called packets, add a destination address, and then pass the packets along to the next protocol layer, the Internet Network layer.

The Internet Network layer encloses the packet in an Internet Protocol (IP) datagram, puts in the datagram header and trailer, decides where to send the datagram (either directly to a destination or else to a gateway), and passes the datagram on to the Network Interface layer.

The Network Interface layer accepts IP datagrams and transmits them as frames over a specific network hardware, such as Ethernet or Token-Ring networks.

<img width="1279" alt="Screen Shot 2023-03-13 at 5 24 16 PM" src="https://user-images.githubusercontent.com/87101785/224764069-84c5588b-7c43-47d0-9acc-d839623a98a4.png">




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
-----------------------------------





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



------------------------------------------------------------------------------------------


HTTP : Hyper-text-Transfer-Protocol basically responsible for communication between web servers and clients, it is the protocol of the web, so every time you open your browser and you visit a web-page or you submit a form, or you click a button than sends some kind of ajax request or fetch request, something like that you are using HTTP and you are going through what is called the request and response cycle. You make a requeste and you get a response back that has something called headers and something called the body, and we are going to look more into that cycle in a bit.

http is stateless, meaning that every request is completely independent, when you make one request visiting a web page or go to another page after that,
or reload the page it dosent remember anyting about the previous, you can kind of look at each request as a single transaction.

HTTPS: Hyper-text-Transfer-Protocol-secure(Data sent is encrypted) it basically where all the data that is sent back is encrypted by something called SSL which stands for secure sockets layer or by TLS which is transport security layer, so anytime you have users that are sending sensitive information 

it should always be over https especially if it is like credit card data, social security numbers, you want to have a hight level of security for that stuff.

A lot of websites and applications now are just forcing https on every page which is a bad idea, you can do this by installing an ssl certificate on your web host, there is different level of security.


Al right when a request is made to a server it has some kind of method attached to it, and there is more than this .


GET: a get request is used to get or fetch data from the server, it could be just loading a standard HTML page, loading assets like CSS or images JSON data XML data, so everytime you visit a webpage you are making a get request to the server via HTTP.

POST: post request is usually used when you are posting data or when you are adding something to the server(adding a ressource) or when you submit a form like let's say a contact form you will be making a post request, if you are submitting maybe a blog post or creating a blog post that is gonna be a POST request, you are sending data to the server and typically that data will be stored in a database somewhere. we can also have forms that make GET request but it is less secure.

PUT : put request which is used to update data that is already on the server so if you have a blog post you want to edit it, maybe change the image or change some text, typically you do that with a put request.


Delete: delete request just delete data from the server.





With each request and response using HTTP  we have something called the header and something called the body

<img width="937" alt="Screen Shot 2023-03-13 at 2 50 42 PM" src="https://user-images.githubusercontent.com/87101785/224721630-8d929d10-09e8-4aac-ae19-8ecd68716fab.png">


The body typically with a response is going to be the html page that you are trying to load  the json data whatever is being sent from the server and then when you make a request you can also send a request body for instance when you submit a form, the form fields you are submitting are part of the request body.

When you comes to the header you also have a request headers and response headers in something called a general header, it is basically divided into three parts and there is different fields on each parts 

<img width="2390" alt="Screen Shot 2023-03-13 at 3 06 39 PM" src="https://user-images.githubusercontent.com/87101785/224725654-6b07a55c-48b8-41d2-9dce-065024d1aef9.png">

A header will look something like this, you will make a (Method like a GET request)(Path or URL)(with aprotocol in this case http) and have all this different header fields and a lot of this you are not really  going to care about but it is good to know what some of the more common ones 
do and what they are especially with the general part of it.

so in general we have --->

request URL: It is just the URL you are requesting 

Request Method : so if it is a get request, post request .....

Statues code: it is probably the most important 

Remote address: which is the ip of the remote computer.

Referrer Policy: if you go to a page from another page it might have some information and that and whatever the poll referrer policy  is.



In Response we have --->

server : so if it is apache or nginx or something like that, and a lot of times this will be hidden just to prevent hackers from knowing what type of server the website uses.

Set-Cookies : is used for servers to send small pieces of data called cookies from the server to the client.

content type : so every response has a content type for instance if it is an html page it will have a content type of text/html, css files would be test/css, images will have image/png or image/jpeg.

Content-Length: Content length which is just that it is the length, it is in octets.

In request we have --->

Cookies: if you have a cookie that was previously sent by the server and you need to send it back to the server you would do it in this field 

Accept-xxx: Like accepting coding, accepting character set , accepting language.

Content-Type: if you are sending data like lets say you are sending json, you had want to set this to application/json

Content-Length: 

Authorization: remember that http is stateless so you might need to send some type of token withing the header , the authorization and the header so that you can for instance validate a user to access a protected route or a protected page, unless you are using something like session on the server .

User-Agent: is typically a long string that has to do with the software that the user is using the operating system, the browser think like that .

Referrer: referrer has info regarding the referring site, if you are to click on a link or whatever

------------------------------------------------------------------------



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


https://www.youtube.com/watch?v=iYM2zFP3Zn0

https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server

https://www.youtube.com/watch?v=_0thnFumSdA&t=41s
