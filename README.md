# Webserv-explination






🌱 1. How internet works
-------------------------

The Internet is the backbone of the Web, the technical infrastructure that makes the Web possible. At it's most basic, the Internet is a large network of computers which communicate all together.


Deeper dive:

A simple network

When two computers need to communicate, you have to link them, either physically (usually with an Ethernet cable) or wirelessly (for example with Wi-Fi or Bluetooth systems). All modern computers can sustain any of those connections.

<img width="639" alt="Screen Shot 2023-03-14 at 6 17 16 PM" src="https://user-images.githubusercontent.com/87101785/225086696-5bb1907e-d76f-4b43-a92a-32c87ec40baa.png">

Such a network is not limited to two computers. You can connect as many computers as you wish. But it gets complicated quickly. If you're trying to connect, say, ten computers, you need 45 cables, with nine plugs per computer!

<img width="639" alt="Screen Shot 2023-03-14 at 6 20 11 PM" src="https://user-images.githubusercontent.com/87101785/225086710-fbb0ce41-849a-4ed3-85e4-aa6691b2a3b8.png">


To solve this problem, each computer on a network is connected to a special tiny computer called a router. This router has only one job: like a signaler at a railway station, it makes sure that a message sent from a given computer arrives at the right destination computer. To send a message to computer B, computer A must send the message to the router, which in turn forwards the message to computer B and makes sure the message is not delivered to computer C.

Once we add a router to the system, our network of 10 computers only requires 10 cables: a single plug for each computer and a router with 10 plugs.

<img width="639" alt="Screen Shot 2023-03-14 at 6 22 37 PM" src="https://user-images.githubusercontent.com/87101785/225087284-f47815f2-2574-438c-a57b-a9068e3e4f0d.png">



<img width="639" alt="Screen Shot 2023-03-14 at 6 34 34 PM" src="https://user-images.githubusercontent.com/87101785/225090304-98770158-9cb2-4e2a-a033-231729fcbd41.png">




🌱 2 : Web server
-----------------

2.1-What is web server?
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




---------------------------------------------------------------------------------------------------------------

What is a web server ?


and what kind of applications are used to serve web applications?


From a hardware standpoint anything with a network connection could be  a web server; your laptop, a smartphone...... .



------->A web server is really just piece of software that serves web content.

So the six things that a webserver does in roughly the order in which they happen, so to serve a web content a web server 

listens on a port for a request sent via a transport protocol and returns a response containing the requested resource 



1: listen

2: on a port

3: For a request

4: Transport protocol

5: response

6: resource


so lets go ahead nd take each one of these items one by one 



Firstly let's focus for a minute on what it means for a web server to listen, basically once a web server application starts up, it just sits there 

waiting for uncoming request , if no request comming then the web server doesnt actually do anything 

now i happen to have a web server running right now on my local machine, of course it is running on the local host ip address (http://127.0.0.1).

so what exactly is the webserver listening to --> The answer is a network port provided by the operating system that the web server is running on, more specifically the network protocol that we are using provides 65.535 ports that software running on the computer can communicate over.

now when a web server starts up it begins listening or if so configured many of thos ports going back 

when we taped the ip address 127.0.0.1 we didnt provide a ports and that is because a web browser automatically sends a web request to either port 80 or port 443, depending on whether we prefix the url with http or https. 



This is an HTTP request example:

<img width="777" alt="Screen Shot 2023-03-21 at 1 22 12 PM" src="https://user-images.githubusercontent.com/87101785/226618914-f0a90d7f-f2a4-4d53-b3c1-c6894ef6b8dc.png">


<img width="777" alt="Screen Shot 2023-03-21 at 1 35 34 PM" src="https://user-images.githubusercontent.com/87101785/226622480-60803eb4-e1d2-4dac-a982-63182723eb96.png">


The first line is the start line which contains, the request method (GET) then the request target which is the spesific web page (/orders/123) 
or resource we are requesting, and finally the http version 1.1

The second line is the ip and port we are attempting to send the request to 

The third line is the user-Agent which is the header that tells the web server, what type of browser we are using  


Finally the fourth block is made up of an optional body which begins, after that first line break






----------------------------------------------------------------------------------------------------------------------------------------------



2.2-Examples of web server software
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


Nginx:
-------


What exactly is NGINX ?   and   What it is purpose is ? 


The best way to say this ---> is to show an example where nginx is being used

so lets going to go to my browser and going to this pages airbnb.ca so you can see that my browser is served a bunch of different content 

<img width="777" alt="Screen Shot 2023-03-22 at 10 01 03 AM" src="https://user-images.githubusercontent.com/87101785/226868585-10306052-b009-4100-af26-1dcd902d2836.png">



we have images ......


The question is how did my browser get all of this content ?

in order to understand this we actually dissect this by inspecting it , and looking at the network tabs 


<img width="777" alt="Screen Shot 2023-03-22 at 10 04 32 AM" src="https://user-images.githubusercontent.com/87101785/226869304-8d1b7921-6338-490c-999a-532d74803d8a.png">

and refresh , and as soon as i refresh you can see here a bunch of a different networks


<img width="777" alt="Screen Shot 2023-03-22 at 10 06 07 AM" src="https://user-images.githubusercontent.com/87101785/226869736-ad0d670b-16e4-4d80-972f-a1d6d0c4a9dd.png">


The first one is our network requests that were made from the browser to a particular server in order to get content, now im going to go ahead and click on the very first network request just to get a little bit more information about it 

<img width="793" alt="Screen Shot 2023-03-22 at 10 08 31 AM" src="https://user-images.githubusercontent.com/87101785/226873400-feb0f07e-d444-4831-a1a1-2fa9768a27f9.png">


we see here a bunch of information and we see also the server section that is actually nginx, so nginx was the one that served us content(served us this web content to our browser )

so nginx is a server that is going to serve web content to our browser 


Lets see an example:


<img width="826" alt="Screen Shot 2023-03-22 at 10 18 37 AM" src="https://user-images.githubusercontent.com/87101785/226873432-95e354ba-26f9-42ad-a3d1-ae1c11366213.png">


lets see i am on my computer and i go to airbn.com now typically what we would think would happen is we make a request over the internet to a server that airbnb is hosting. i'm pretty sure airbnb uses aws, so lets say there is a server on aws that it is nginx.

ans once we make a request it is going to process a request and send back a response 







🌱 3 .What is TCP/IP ?
-----------------------

Une suite de protocoles (organisée en couche) utilisés pour le transfert des données sur internet.

C'ést a dire lorsque deux ordinateur veulent communiquer entre eux via internet, les données echangées vont être mises en forme selon des règles qui sont toujours les mêmes afin que chaque machine puissent se comprendre et que le transfert des données soient fiables. Et pour bien comprendre le fonctionnement, on va voir que le TCP/IP et trés facilement comparables a l'envoi de courrier par la poste. Alors par ailleurs, sacher qu'il ya plusieur facons de voir le TCP/IP et pour ma part, j'ai choisi de présenter un modèle en 4 couche.Et le nom de TCP/IP, acronyme de Transfer Control Protocol et internet Protocol  est en réalité le nom des protocoles qui sont le plus souvent utilisés dans la deuxième et la troisième couche.


<img width="530" alt="Screen Shot 2023-03-14 at 10 27 36 AM" src="https://user-images.githubusercontent.com/87101785/224956594-612ce051-2a22-47c7-88cb-b12ed44497c0.png">





Lorsqu'un message arrive dans un ordinateur, de savoir a quelle application s'addresse le message. Par example, le port 80 identifie une application de serveurs web. La machine elle même doit être identifiée, on utilise pour cela la fameuse adresse IP, elle permet, alors de l'acheminement de  données sur le réseau, de déterminer á chaque embranchement, en fonction de cette adresse IP, de savoir quel chemin emprunter.


<img width="2539" alt="Screen Shot 2023-03-14 at 11 11 17 AM" src="https://user-images.githubusercontent.com/87101785/224969414-f420265b-fdf4-4b61-a6c8-f842e16e575f.png">


Enfin, chaque carte réseau qui permet de brancher l'ordinateur au réseau possède elle aussi une identificateur ->l'adresse MAC(Media access control) qui est l'adresse physique d'une machine, Elle permet dans un reseau d'identifier de manière unique.



Supposont que depuis notre navigateur web, nous voulons afficher la page web de facebook.

Plus detaillé:


Sur votre ordinateur on tape www.facebook.com puis Enter, la couche application va traduire cette requête par "GET" qui signifier (obtenir) suivi de l'adresse du site web sous forme d'adresse IP(by using DNS).

<img width="629" alt="Screen Shot 2023-03-14 at 11 36 48 AM" src="https://user-images.githubusercontent.com/87101785/224974651-40711a39-a90c-4a97-91e1-b449963f3732.png">


Dans notre ordinateur les données sont traitées par la couche "transport" qui va ajouter une en tête avec la port source, vous souvenez c'est le numéro qui identifier les applications, ici le port 1337 identifier notre navigateur web, Il est ajouté le port de destination (80 c'est celui qui identifier une application de serveur web) le message est numéroté et il est prévu un FLAG ou (drapeau) en francais qui servira pour l'accusé de reception,( Ici cette case est pour le moment inutilisée). A ce niveau là, on dit que les données ont été encapsulées, c'est a dire que l'on a ajouter une entête "transport" au message "GET http". 


<img width="629" alt="Screen Shot 2023-03-14 at 11 42 48 AM" src="https://user-images.githubusercontent.com/87101785/224976220-9435ddaa-6d07-4e47-b987-abdd5edc254a.png">

Ce nouvel ensemble de données est alors appelé un "Segment"

<img width="629" alt="Screen Shot 2023-03-14 at 12 10 29 PM" src="https://user-images.githubusercontent.com/87101785/224983522-f8098860-01eb-4380-a777-821dfc1bb797.png">

Dans l'ordinateur, le segment est encapsulé par la couche 2 "internet" qui ajoute l'adresse IP de destination(Dont cette cas c'est l'adresse IP du serveur qui héberge la page web du site facebook) et l'adresse IP source (C'est a dire l'adresse IP de notre ordinateur). A ce niveau, l'ensemble de cette données et appelée "paquet". 

<img width="629" alt="Screen Shot 2023-03-14 at 12 15 43 PM" src="https://user-images.githubusercontent.com/87101785/224984687-76f1a525-771f-4b5b-8e79-3cbb3d92b3a7.png">


La couche réseau encapsule le paquet en lui ajoutant une entête avec l'adresse MAC de la carte réseau de destinations du prochain routeur et l'adresse MAC de la carte réseau de notre ordinateur, et ici on a ce que l'on appelle une "Trame". Alors, voyons la suite ou les messages


<img width="1772" alt="Screen Shot 2023-03-14 at 12 20 24 PM" src="https://user-images.githubusercontent.com/87101785/224985821-3968746f-1e6e-4433-8c6e-d2ffb5e9243a.png">




En bas notre trame quitte notre ordinateur et arrivent au premier routeur, la carte reseau du routeur a son adresse MAC ici


<img width="1826" alt="Screen Shot 2023-03-14 at 2 36 22 PM" src="https://user-images.githubusercontent.com/87101785/225018286-76afee95-2b9a-4eb2-b202-d99055964fd4.png">





et quand l'adresse MAC de destination est bonne , la trame est désencapsulée et l'adresse IP de destination est lue 


<img width="1826" alt="Screen Shot 2023-03-14 at 2 36 06 PM" src="https://user-images.githubusercontent.com/87101785/225018394-48f5f077-dc54-43c7-8b72-3ae6cfd4287b.png">

Alors le paquet est a nouveau  encapsulé et l'adresse MAC src est ajoutée ainsi que l'adresse MAC du prochain routeur.


<img width="1826" alt="Screen Shot 2023-03-14 at 2 41 31 PM" src="https://user-images.githubusercontent.com/87101785/225019721-c296a409-3eed-4519-b1d7-83f7b5d55de1.png">

Alors pour information, les prochaine adresse MAC sont connus par le routeur (grace a ca table de routage) .

En suit la TRAME voyage et arrive au routeur suivant. L'adresse MAC est identifier 

<img width="1826" alt="Screen Shot 2023-03-14 at 2 52 19 PM" src="https://user-images.githubusercontent.com/87101785/225023026-eb8c2301-d93a-4497-a8a3-9aff815d91ef.png">

la trame est donc désencapsulée, 


<img width="1826" alt="Screen Shot 2023-03-14 at 2 55 08 PM" src="https://user-images.githubusercontent.com/87101785/225023736-e7022eed-6be6-4a89-8330-968ffe89ea78.png">





la lecture de l'adresse IP de destination entrain une nouvelle encapsulation ou est ajoutée l'adresse MAC de la carte reseau source et celle de destination 


<img width="1826" alt="Screen Shot 2023-03-14 at 2 54 53 PM" src="https://user-images.githubusercontent.com/87101785/225023770-38971ce8-e2ad-4004-b5c6-3d2093cde62b.png">

<img width="1826" alt="Screen Shot 2023-03-14 at 2 57 44 PM" src="https://user-images.githubusercontent.com/87101785/225024382-b8ad5301-dbdc-4f65-8dac-0a2db6954d93.png">


aprés notre trame arrive dans le serveur de facebook, dans le serveur, comme l'adresse MAC correspond á celle de la carte réseau , la trame est désencapsulée et remontre vers la couche internet 

<img width="2174" alt="Screen Shot 2023-03-14 at 3 01 46 PM" src="https://user-images.githubusercontent.com/87101785/225025419-9ffd538e-7cf9-4bad-97a1-8e5f578fbc88.png">

dans notre serveur l'adresse IP etant bien celle de destination

<img width="502" alt="Screen Shot 2023-03-14 at 3 04 38 PM" src="https://user-images.githubusercontent.com/87101785/225026137-47d62a57-c044-4ac4-8d03-366c1ed9a9b8.png">

le paquet est cette fois, lui aussi désencapsulé et remonte vers la couche transport  

<img width="502" alt="Screen Shot 2023-03-14 at 3 06 22 PM" src="https://user-images.githubusercontent.com/87101785/225026655-733f3561-d914-41ad-a7de-67caf64cbea9.png">

La couche transport voire que les données sont adressées au port 80, c'ést a dire je vous rappele l'application du serveur web, le segment est alors desencapsulé et remonte a la couche application  

<img width="502" alt="Screen Shot 2023-03-14 at 3 09 16 PM" src="https://user-images.githubusercontent.com/87101785/225027493-74dddca0-c892-49ec-8c04-b76faa3fc531.png">


et a la fin la couche application transmet la requete a l'application du serveur web.


Alors ! Les message sont arrivés au destinataire







mais comment l'expéditeur va t-il le savoir?


les port source et destination sont inversés, le numero du message est augmenté de 1, donc il passe a 2, c'est la manière de savoir que l'accusé de réception fait suite aux messages précédents, et le FLAG va être maintenant utilisé en y inscrivant ACK qui signifie en anglais (Acknowledgment)

<img width="502" alt="Screen Shot 2023-03-14 at 3 33 04 PM" src="https://user-images.githubusercontent.com/87101785/225034360-dc7f859e-d5c7-4060-955f-3fd49779c456.png">

<img width="502" alt="Screen Shot 2023-03-14 at 3 33 36 PM" src="https://user-images.githubusercontent.com/87101785/225034559-a6c99cd1-7fa9-4a07-83ec-1dbbc5e29b47.png">

<img width="502" alt="Screen Shot 2023-03-14 at 3 33 50 PM" src="https://user-images.githubusercontent.com/87101785/225034571-d2ad2542-4af5-4459-b451-c41903db77b2.png">


c'ést a dire "accusé de réception", sous entendu -->"jai bien recu le message".

Alors ce message est vide, vous aurez remarqué ici que la partie "application" est vide c'est seulement l'enveloppent qui va voyager donc ce message vide va être a son tour encapsulé par la couche internet 

<img width="502" alt="Screen Shot 2023-03-14 at 3 36 26 PM" src="https://user-images.githubusercontent.com/87101785/225035307-dfd3c2b4-1edf-48b6-830a-d0b3ce82f830.png">


et aprés l'adresse IP de destination est inversée avec l'adresse IP source 



<img width="502" alt="Screen Shot 2023-03-14 at 3 39 02 PM" src="https://user-images.githubusercontent.com/87101785/225036071-a61a70ee-c764-49b2-ac59-70db9307db4f.png">





et puis le  paquet est encapsulé par la couche "réseau"


<img width="1606" alt="Screen Shot 2023-03-14 at 3 40 11 PM" src="https://user-images.githubusercontent.com/87101785/225036537-e3608c02-a288-45c9-b5ad-8b8778a4b527.png">


aprés l'adresse MAC sont mis a jour puis la trame repart sur réseau internet jusqu'a notre ordinateur


<img width="1606" alt="Screen Shot 2023-03-14 at 3 42 08 PM" src="https://user-images.githubusercontent.com/87101785/225056398-26f3017f-fca4-4504-94bf-5cb13f34c8cc.png">





<img width="2523" alt="Screen Shot 2023-03-14 at 3 43 31 PM" src="https://user-images.githubusercontent.com/87101785/225037539-23728bbe-cbce-4199-9e30-4fdfbbbef906.png">




------------------------------------------------------------------------------------------------------------------------

TCP/IP stands for Transmission Control Protocol/Internet Protocol and is a suite of communication protocols used to interconnect network devices on the internet. TCP/IP is also used as a communications protocol in a private computer network (an intranet or extranet).

TCP defines how applications can create channels of communication across a network. It also manages how a message is assembled into smaller packets before they are then transmitted over the internet and reassembled in the right order at the destination address.






levels:

<img width="594" alt="Screen Shot 2023-03-13 at 11 40 29 AM" src="https://user-images.githubusercontent.com/87101785/224678598-0ee5e092-87ee-4f82-9a25-de47e4ae8cf9.png">



TCP/IP carefully defines how information moves from sender to receiver. First, application programs send messages or streams of data to one of the Internet Transport Layer Protocols, either the User Datagram Protocol (UDP) or the Transmission Control Protocol (TCP). These protocols receive the data from the application, divide it into smaller pieces called packets, add a destination address, and then pass the packets along to the next protocol layer, the Internet Network layer.

The Internet Network layer encloses the packet in an Internet Protocol (IP) datagram, puts in the datagram header and trailer, decides where to send the datagram (either directly to a destination or else to a gateway), and passes the datagram on to the Network Interface layer.

The Network Interface layer accepts IP datagrams and transmits them as frames over a specific network hardware, such as Ethernet or Token-Ring networks.

<img width="1279" alt="Screen Shot 2023-03-13 at 5 24 16 PM" src="https://user-images.githubusercontent.com/87101785/224764069-84c5588b-7c43-47d0-9acc-d839623a98a4.png">




🌱 4.What is OSI?
-----------------

The OSI reference model defines how applications can communicate over a network.


TCP connection establishment :
--------------------------------

When two hosts communicate using tcp , a connection is established before data can be extchanged.

To establish the connection, hosts use a three-way handshake flagging with the SYN and ACK control in the TCP header.

The three-way  handshake:

. Establishes that the destination device is present on the network.

. Verifies that the destination device has an active service and is accepting requests on specified destination port number.

. Both the client and the destination (server) must allocate resources to keep track of the connection - more resource intensive on the server side when it has multiple client.

🌱 5. TCP and UDP sockets:
-------------------------

What is a socket:
-----------------


socket is an endpoint of 2-way communication between programs running on the network


for example:

client program want to communicate with a server program, so it means client program want to send a message to the server program, so how client program will send the message to the server program ? 

as per the definition socket is required when two different programs running on the network, so this is client side socket and this is server side socket


<img width="777" alt="Screen Shot 2023-03-17 at 2 44 58 PM" src="https://user-images.githubusercontent.com/87101785/225922508-0a538310-061b-4f4d-b0d2-73c712f1009c.png">


the socket address is associated  with the ip address as well as the port address. so this is the client IP address and this is the server IP address



<img width="777" alt="Screen Shot 2023-03-17 at 2 46 30 PM" src="https://user-images.githubusercontent.com/87101785/225922921-73b106fb-6455-4ef6-9560-255db253e76d.png">

so here client and server can send the data through the IP address 

Here there is client side ports and server side ports 


<img width="777" alt="Screen Shot 2023-03-17 at 2 57 17 PM" src="https://user-images.githubusercontent.com/87101785/225925803-47a4075c-22f9-48fa-bec9-d4eab21d6ad8.png">


so the socket address is associated with the ip address and the port address, in this senario client want to send a message to the server so first of all client will shoose any free port which is available at the server (the same thing for the server).


so client program send that message to the socket and socket will forward that message to the selected port of the client machine, so client side selected port forward that message to the agreed port to the server, now that agreed port forward that message to the socket, and socket will pass that message to the respected program running on the server side. 

---------------------------------------------------------------------------------------------------------------------------------------

Socket used for communication between client and server systems.

so lets see what is this sockets ?

how do they work ?

how do they help in communication between two or more processes?


1: socket identified by an IP address followed by a port number.

2: The server waits for incoming client requests by listening to a specified port. Once a request is received,the server accepts a connection from the client socket to complete the connection.


ps: what is the client and server?

In a client server systems, the client asks for information from the server and the server will give that information to the clients, that how is works. so in order for the client to communicate to the server and the server to communicate back to the client, there needs to be a connection
between the client and the server, so in order to establish this connection we are going to use a sockets.





--------------------------------------------------------------------------------------------------------------------------------------------------------

In this example we have two clients connected to the same web server and just so happens they are both using the same port numbers 
49888

<img width="753" alt="Screen Shot 2023-03-16 at 9 26 33 AM" src="https://user-images.githubusercontent.com/87101785/225558182-415251fe-9300-4fa5-a0ef-5b0e5759af9f.png">

So how does the server know which port number to associate with what which device ?

What makes each connection unique ?

okey

the way that it does this is the connection is divided defined by a pair of numbers known as sockets

the source IP address and source port from the client to the server and the destination IP address and destination port number server, but this is all from the perspective of whoever we are looking at, so from the source IP address and source port number this is where the segment coming from,
it is coming from this IP address and this specific port on the client.

--->So combining the transport layer port number and the network layer address uniquely identifies a particular application process running on an individual host device.

"This combination is called a socket."

--> A socket pair, consisting of the source and destination IP addresses and port numbers, is also unique and identifies the specific conversation between the two hosts.


Let's take an example:


A client socket look like this, representing the source IP address and source port number

192.168.1.101:49888

<img width="753" alt="Screen Shot 2023-03-16 at 9 55 04 AM" src="https://user-images.githubusercontent.com/87101785/225564930-51ba1ac8-99ed-4f4c-8b19-09d3a0683695.png">


So this is the client socket with the source IP address and the source port number, this identifies the where the application came from, it come from a spesific IP address.

The socket on a web server might be, representing the destination IP adddress and destination port number 

192.133.219.25:80

<img width="753" alt="Screen Shot 2023-03-16 at 9 58 55 AM" src="https://user-images.githubusercontent.com/87101785/225565958-3a37fb48-8014-429b-900a-e2c684f206ff.png">

--->Together, these two sockets combine to form a socket pair 192.168.1.101:49888 ,  192.133.219.25:80 


netstat -n command shows us this socket pair so it shows us any of the TCP and UDP processes that we have currenty running on our system 

<img width="601" alt="Screen Shot 2023-03-16 at 10 08 04 AM" src="https://user-images.githubusercontent.com/87101785/225568351-27c259d7-4ab2-4fd5-aff4-48bfa2ed5617.png">




 The server creates a socket, attaches it to a network port addresses then waits for the client to contact it. The client creates a socket and then attempts to connect to the server socket. When the connection is established, transfer of data takes place.
 
<img width="1975" alt="Screen Shot 2023-03-16 at 10 08 48 AM" src="https://user-images.githubusercontent.com/87101785/225568595-2622f3ac-50bc-4ff8-9458-387edef2072e.png">

<img width="650" alt="Screen Shot 2023-03-16 at 10 50 26 AM" src="https://user-images.githubusercontent.com/87101785/225579973-504be38b-deaa-4440-827e-4252c8e4e8a6.png">


5.1 Types of sockets
-----------------


Types of Sockets : There are two types of Sockets: the datagram socket and the stream socket.


Datagram Socket : This is a type of network which has connection less point for sending and receiving packets. It is similar to mailbox. The letters (data) posted into the box are collected and delivered (transmitted) to a letterbox (receiving socket).


Stream Socket : In Computer operating system, a stream socket is type of interprocess communications socket or network socket which provides a connection-oriented, sequenced, and unique flow of data without record boundaries with well defined mechanisms for creating and destroying connections and for detecting errors. It is similar to phone. A connection is established between the phones (two ends) and a conversation (transfer of data) takes place.



🌱6. What happens when tou type a URL into your browser?
---------------------------------------------------

Here Bob enters a URL into the browser and click Enter.


<img width="460" alt="Screen Shot 2023-03-16 at 11 07 10 AM" src="https://user-images.githubusercontent.com/87101785/225584186-3a3f8653-a778-486d-a1cc-3462fac3654d.png">


What happens next?

Let's first discuss what a URL is ?  URL stands for (universal resource locator), and it has four parts:

<img width="610" alt="Screen Shot 2023-03-16 at 11 13 25 AM" src="https://user-images.githubusercontent.com/87101785/225585757-285de5a4-a166-4b97-b745-c1f0254a167a.png">


They together specify the resource on the server we want to load.



so okey Let's continue ----->

Bob entered the URL into the browser, what happend next, Well the browser needs to know  how to reach the server, in this case "example.com".

This done with a process called DNS lookup (DNS stands for Domain Name system) think of it as a phone book of the internet. DNS translates domain names to IP addresses so browsers can load resources. It is an interesting service in and off.

Finally the browser has the IP address of the server, in our case again example.com, next the browser establishes a TCP connection with the server using the IP address it got for it.

<img width="557" alt="Screen Shot 2023-03-16 at 11 23 35 AM" src="https://user-images.githubusercontent.com/87101785/225588125-c4b729d7-9a08-4f2a-bd8a-ef4dfd3e2b6b.png">



Now there is a handshake involved in establishing a TCP connection. It takes several network round trips for this to complete. To keep the loading process fast, modern browsers use something called a keep alive connection to try to reuse an established TCP connection to the server as much as possible.

one thing to note is that if the protocol is https the process of establishing a new connection is even more involved. It requires a complicated process called SSL/TLS handshake to establish the encrypted connection between the browser and the server.

Finally the browser sends an HTTP request to the server over the established TCP connection 

<img width="557" alt="Screen Shot 2023-03-16 at 11 30 21 AM" src="https://user-images.githubusercontent.com/87101785/225589841-42a8dfed-c880-44c7-a79e-3020c810acaa.png">


HTTP is a very simple protocol. The server processes the request and sends back a response 

<img width="557" alt="Screen Shot 2023-03-16 at 11 31 20 AM" src="https://user-images.githubusercontent.com/87101785/225590097-1d9664da-ff6d-4e74-9abd-771573ea13b7.png">


The browser receives the response and renders html content

<img width="679" alt="Screen Shot 2023-03-16 at 11 32 07 AM" src="https://user-images.githubusercontent.com/87101785/225590339-2d4a4c01-4748-4a40-a788-fa2891b1b7ea.png">


 🌱 7. What is HTTP?
----------------------

The Hypertext Transfer Protocol (HTTP) is the foundation of the World Wide Web, and is used to load webpages using hypertext links. HTTP is an application layer protocol designed to transfer information between networked devices and runs on top of other layers of the network protocol stack. A typical flow over HTTP involves a client machine making a request to a server, which then sends a response message.


C'est un protocole la plus utiliser sur internet, il pêrmet un navigateur d'obtenir des page web.

le navigateur web est une application client qui accède aux ressources stockees sur un serveur web.

Lorsque une URL est saisie au niveau des navigateur web client, le client http envoyer un requête http au serveur, le protocole http au niveau de serveur http s'éxecute en arriere plan, donc il s'agie d'un service, donc ce service il va traiter la requête http et il envois ce que n'appele une reponse http.


 🌱8. La structure d'une requite HTTP:
--------------------------------------





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



 🌱 8.1 example:
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


Hypertext Transfer Protocol (HTTP) is an application-layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers, but it can also be used for other purposes. HTTP follows a classical client-server model, with a client opening a connection to make a request, then waiting until it receives a response. HTTP is a stateless protocol, meaning that the server does not keep any data (state) between two requests.



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



🌱 9: Protocoles:
-----------------


9.1: What is protocole:
----------------------

a protocol can be defined as a set of rules convensions and data structures that dictate how devices extchange data across a networks. In other words network protocols can be equated to languages that two devices most understand for seamless communication of information, regardless of their infrastructure and design desparities.

A network protocol is an established set of rules that determine how data is transmitted between different devices in the same network. Essentially, it allows connected devices to communicate with each other, regardless of any differences in their internal processes, structure or design. Network protocols are the reason you can easily communicate with people all over the world, and thus play a critical role in modern digital communications.

Similar to the way that speaking the same language simplifies communication between two people, network protocols make it possible for devices to interact with each other because of predetermined rules built into devices’ software and hardware. Neither local area networks (LAN) nor wide area networks (WAN) could function the way they do today without the use of network protocols.


Protocols are sets of rules for message formats and procedures that allow machines and application programs to exchange information. These rules must be followed by each machine involved in the communication in order for the receiving host to be able to understand the message.

9.2: List of Network Protocols:
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

🌱10. What is NGINX:
--------------------

nginx [engine x] is an HTTP and reverse proxy server.


Nginx act like a proxy --> Load balancing , backend routing, Caching 

and a web server --->  Serves web content



web server controls how users access the application through HTTP request (accessing a website means making a request to server) and NGINX is known to handle more than 10.000 requests at once), so a lot of companies like google, facebook, and linkdin are known to use nginx as their web server because they have a lot of users trying to access their services at once, onother cool aspect of nginx is that it works a reverse proxy server, that means a direct client is request to the appropriate applications.




10.1 Why Nginx called a reverse proxy ?
--------------------------------------


What is a proxy anyways?

<img width="607" alt="Screen Shot 2023-03-16 at 2 28 13 PM" src="https://user-images.githubusercontent.com/87101785/225631753-d30b04fd-2fcd-4fa8-add7-37a0376934a0.png">

There is two common types pf proxy are forward proxy and reverse proxy :



📈 Forward proxy:

a forward proxy is a server that sits between a group of client machines and the internet, when those clients make requests to websites on the internet, the forward proxy acts as a middleman intercepts those requests and talks to web servers on behalf of those client machines.

Why would anyone want to do that ?

Here are a few common reasons:

1. a forward proxy protects the client is online identity, by using a forward proxy to connect a website, the IP address of the client is hidden from the server, only the IP address of the forward proxy is visible to the servers, so it would be harder to trace back to the client.

2. a forward proxy can be used to block access to certain content, this is not uncommon for schools and businesses to configure ther networks to connect all clients to the web through a proxy and apply filtering rules to disallow sites like social networks. 

📈 reverse proxy:

A reverse proxy sits between the internet and the web servers, it intercepts the requests from clients and talks to the web server on behalf of the clients

why would a website use a reverse proxy?

1. a reverse proxy could be used to protect a website, the website is IP addresses are hidden behind the reverse proxy and are not relealed to the clients, this makes it much harder to target a DDos attack against a website.

2. a reverse proxy is used for load balancing
 
3. a reverse proxy can balance a large amount of incoming requests by distributing the traffic to a large pool of web servers


🌱11.what is Telnet:
--------------------

Telnet is a terminal emulation program that is used to access remote servers 

<img width="681" alt="Screen Shot 2023-03-16 at 3 30 49 PM" src="https://user-images.githubusercontent.com/87101785/225649618-1748f927-bda2-4227-b614-4dcb2a2de519.png">

it is a simple command line tool that runs on your computer , and it will allow you to send commands remotely to a server and administer that server just as if you were sitting in front of it 

<img width="681" alt="Screen Shot 2023-03-16 at 3 33 16 PM" src="https://user-images.githubusercontent.com/87101785/225650280-4ec064c7-b4fe-428a-817c-d6fa0e663469.png">


so when you connect remotely to a server using telnet, you would just use commands with a keyboard to tell that server what to do . so you can commands to run rograms, create folders, delete files, create files, tranfer files, browse directories, so you can do eveything even if you are a thousand miles away from that server. 


🌱 12.What is CGI:
-----------------

CGI is a standard method used to generate dynamic content on web pages. CGI stands for Common Gateway Interface and provides an interface between the HTTP server and programs generating web content. These programs are better known as CGI scripts. They are written in a scripting language. The Network Component provides such a scripting language. The HTTP server processes the script source file line by line and calls the CGI functions as needed. The output from a CGI function is sent to the web client (browser) as a part of the web page.


🌱 13. what is a proxy server?
-----------------------------

A proxy server is a system or router that provides a gateway between users and the internet.Therefore, it helps prevent cyber attackers from entering a private network.




HTTP server: Everyrhing you need to know to build a simple HTTP server from scratch :
--------------------------------------------------------------------------------------



1:  implementing TCP:

to implement Tcp we have to learn TCP socket programming.

---> programming with TCP/ip sockets:

There are a few steps involved in using sockets

1: Create the socket

2: Identify the socket

3: On the server, wait for an incomint connection

4: Send and receive messages

5: Close the socket


14.Function used in this projects:
-------------------------------

14.1 socket() :
-------------

socket():  int socket(int domain, int type, int protocol);


The socket function is used to create a new socket descriptor 

The socket() function shall create an unbound socket in a communications domain, and return a file descriptor that can be used in later function calls that operate on sockets.


The socket() function takes the following arguments:

domain: Specifies the communications domain in which a socket is to be created.

type:Specifies the type of socket to be created.



Three types of sockets are supported:

Stream sockets allow processes to communicate using TCP. A stream socket provides bidirectional, reliable, sequenced, and unduplicated flow of data with no record boundaries. After the connection has been established, data can be read from and written to these sockets as a byte stream. The socket type is SOCK_STREAM.

Datagram sockets allow processes to use UDP to communicate. A datagram socket supports bidirectional flow of messages. A process on a datagram socket can receive messages in a different order from the sending sequence and can receive duplicate messages. Record boundaries in the data are preserved. The socket type is SOCK_DGRAM.

Raw sockets provide access to ICMP. These sockets are normally datagram oriented, although their exact characteristics are dependent on the interface provided by the protocol. Raw sockets are not for most applications. They are provided to support developing new communication protocols or for access to more esoteric facilities of an existing protocol. Only superuser processes can use raw sockets. The socket type is SOCK_RAW.

protocol:Specifies a particular protocol to be used with the socket. Specifying a protocol of 0 causes socket() to use an unspecified default protocol appropriate for the requested socket type.


14.2: bind() :
------------

int bind(int socket, struct sockaddr *address, int address_len);

(identify (give a name to a socket ) a socket)

The bind() function binds a unique local name to the socket with descriptor socket. After calling socket(), a descriptor does not have a name associated with it. However, it does belong to a particular address family as specified when socket() is called. The exact format of a name depends on the address family.

Parameter:

    Description :
    
socket: The socket descriptor returned by a previous socket() call.

address:The pointer to a sockaddr structure containing the name that is to be bound to socket.

address_len:The size of address in bytes.

14.3: htons():
---------------


The htons function takes a 16-bit number in host byte order and returns a 16-bit number in network byte order used in TCP/IP networks (the AF_INET or AF_INET6 address family).

The htons function can be used to convert an IP port number in host byte order to the IP port number in network byte order.

14.4: htonl():
-------------

The htonl function takes a 32-bit number in host byte order and returns a 32-bit number in the network byte order used in TCP/IP networks (the AF_INET or AF_INET6 address family).

The htonl function can be used to convert an IPv4 address in host byte order to the IPv4 address in network byte order. This function does not do any checking to determine if the hostlong parameter is a valid IPv4 address.


14.5: connect():
--------------

int connect(int socket, const struct sockaddr *address, socklen_t address_len);



For stream sockets, the connect() call attempts to establish a connection between two sockets. For datagram sockets, the connect() call specifies the peer for a socket. The socket parameter is the socket used to originate the connection request. The connect() call performs two tasks when called for a stream socket. First, it completes the binding necessary for a stream socket (in case it has not been previously bound using the bind() call). Second, it attempts to make a connection to another socket.



14.6: poll() && select():
-------------------------

The select() and poll() methods can be a powerful tool when you’re multiplexing network sockets. Specifically, these methods will indicate when a procedure will be safe to execute on an open file descriptor without any delays. For instance, a programmer can use these calls to know when there is data to be read on a socket. By delegating responsibility to select() and poll(), you don’t have to constantly check whether there is data to be read. Instead, select() and poll() can be placed in the background by the operating system and woken up when the event is satisfied or a specified timeout has elapsed.


14.8: listen():
--------------


int listen(int socket, int backlog);

The listen() call indicates a readiness to accept client connection requests. It transforms an active socket into a passive socket. Once called, socket can never be used as an active socket to initiate connection requests. Calling listen() is the third of four steps that a server performs to accept a connection. It is called after allocating a stream socket with socket(), and after binding a name to socket with bind(). It must be called before calling accept().

14.*9: fd_set:
-------------

The fd_set structure is used by various Windows Sockets functions and service providers, such as the select function, to place sockets into a "set" for various purposes, such as testing a given socket for readability using the readfds parameter of the select function.



14.10: accept():
--------------



int accept(int socket, struct sockaddr *address, int *address_len);


The accept() call is used by a server to accept a connection request from a client. When a connection is available, the socket created is ready for use to read data from the process that requested the connection. The call accepts the first connection on its queue of pending connections for the given socket socket. The accept() call creates a new socket descriptor with the same properties as socket and returns it to the caller.

14.11: select():
----------------


The select() call monitors activity on a set of sockets looking for sockets ready for reading, writing, or with an exception condition pending.


--> The select() function indicates which of the specified file descriptors is ready for reading, ready for writing, or has an error condition pending

int select(int nfds, fd_set *readfds, fd_set *writefds, fd_set *exceptfds)

nfds: The number of socket descriptors to be checked. This value should be one greater than the greatest number of sockets to be checked.

readfds :Points to a bit set of descriptors to check for reading.

writefds : Points to a bit set of descriptors to check for writing.

exceptfds: Points to a bit set of descriptors to check for exception conditions pending.

timeout : Points to the time to wait for select() to complete.


14.12: send():
-------------

The send() function sends data on the socket with descriptor socket

int send(int socket, char *buffer, int length, int flags);



15: confif_file NGINX:
---------------------



15.1: location:
---------------


example :


           server 
           {
              root /www/data;

              location / {
              }

              location /images/ {
              }

              location ~ \.(mp3|mp4) {
                root /www/media;
              }
           }
           
           
           
Here, NGINX searches for a URI that starts with /images/ in the /www/data/images/ directory in the file system. But if the URI ends with the .mp3 or .mp4 extension, NGINX instead searches for the file in the /www/media/ directory because it is defined in the matching location block.

If a request ends with a slash, NGINX treats it as a request for a directory and tries to find an index file in the directory. The index directive defines the index file’s name (the default value is index.html). To continue with the example, if the request URI is /images/some/path/, NGINX delivers the file /www/data/images/some/path/index.html if it exists. If it does not, NGINX returns HTTP code 404 (Not Found) by default.



example:
 in this example, if the URL is localhost::8080/fruits so NGINX  delivers the file /Users/souchen/.brew/etc/nginx/mysite/fruits,
 
 exactly in index.html (by default)
 
 
<img width="616" alt="Screen Shot 2023-03-30 at 12 26 16 PM" src="https://user-images.githubusercontent.com/87101785/228836768-889d84f9-4c91-454f-90ad-1ccff680655b.png">


15.2 : alias
-------------

To understand alias lets talk about this example:

Here we will not add /carbs to the link, so if the URL is localhost:8080/carbs , NGINX delivers the file /Users/souchen/.brew/etc/nginx/mysite/fruits,

exacty index.html (by default)


<img width="515" alt="Screen Shot 2023-03-30 at 12 33 20 PM" src="https://user-images.githubusercontent.com/87101785/228837401-ac9fd891-6a39-4c2c-bf8f-8a55f9279e73.png">


but if there is no index.html at that directory !?

<img width="701" alt="Screen Shot 2023-03-30 at 1 08 20 PM" src="https://user-images.githubusercontent.com/87101785/228848980-a6f062a9-0c14-433e-9f89-a66e18e5815e.png">


for example here we have in directory vegetables the file vegetables.html not index.html so if the URL is localhost:8080/vegetables, NGINX delivers the file 404 error

so we will fix this problem by using try_files


<img width="701" alt="Screen Shot 2023-03-30 at 1 24 02 PM" src="https://user-images.githubusercontent.com/87101785/228850426-79e3c72b-3f75-4b86-bf37-d79210e22f91.png">



try_files means --> try this files if it exist go for it  but if not exist we should throw 404 error


<img width="701" alt="Screen Shot 2023-03-30 at 1 27 28 PM" src="https://user-images.githubusercontent.com/87101785/228851345-332b4737-f157-485a-a7ac-bd9910e12771.png">




15.3: root
-----------

The root directive specifies the root directory that will be used to search for a file. NGINX appends the request URI to the path specified by the root directive. 

      server {
          root /www/data;
      }
      
15.4: autoindex
--------------

To configure NGINX to return an automatically generated directory listing instead, include the on parameter to the autoindex directive:

        location /images/ {
            autoindex on;
         }


15.5: index
-----------


To return the index file, NGINX checks for its existence and then makes an internal redirect to the URI obtained by appending the name of the index file to the base URI. The internal redirect results in a new search of a location and can end up in another location as in the following example:


     location / {
    root /data;
    index index.html index.php;
    }


15.6: include
------------

<img width="826" alt="Screen Shot 2023-03-30 at 11 57 47 AM" src="https://user-images.githubusercontent.com/87101785/228829266-3dc6b81d-39ad-427a-9e74-f0f013cda412.png">

here we can replace type with  include because we can have more than two types of files, and we find this all types in mime.types file


This is mime.types file -->

<img width="616" alt="Screen Shot 2023-03-30 at 12 04 01 PM" src="https://user-images.githubusercontent.com/87101785/228830154-3cddd574-1ff0-4af5-b9d8-f50f6ae1ed0b.png">


so we can replace type with include -->


<img width="616" alt="Screen Shot 2023-03-30 at 12 03 47 PM" src="https://user-images.githubusercontent.com/87101785/228830375-6d4bee2d-f1e9-4eda-ad2b-8aef3edbdc2d.png">



15.7: Redirects and Rewrites:
----------------------------

15.7.1 Redirects:
---------------

15.7.1.1 return
---------------

As you see we dont have directory meals in our project


<img width="701" alt="Screen Shot 2023-03-30 at 2 07 14 PM" src="https://user-images.githubusercontent.com/87101785/228862772-34a7a9c9-cf1a-47b4-aa17-586aa67b2145.png">

so if the request URL is localhost::8080/meals  NGINX delivered the file /Users/souchen/.brew/etc/nginx/mysite/fruits



thet why we will going to return a 307 /fruits (to redirect /fruits file)

<img width="701" alt="Screen Shot 2023-03-30 at 2 05 51 PM" src="https://user-images.githubusercontent.com/87101785/228862510-96e8fcb6-972c-4ccf-99d9-3601e964968d.png">

15.7.1.2 rewrite:
----------------



here when i tape the URL localhost:8080/number/2  NGINX delivere  the same file that will delivere when the URL is localhost:8080/count/2


<img width="519" alt="Screen Shot 2023-03-30 at 2 20 39 PM" src="https://user-images.githubusercontent.com/87101785/228867540-81683a59-6f9b-4e68-a885-0b48d02b9ccd.png">



16: How we can reload NGINX as load balancer:
---------------------------------------------

Firsty what is a load balancer :

When our application starts getting a lot of users 


<img width="660" alt="Screen Shot 2023-03-30 at 2 28 16 PM" src="https://user-images.githubusercontent.com/87101785/228868919-c1137a96-d871-41ac-ba7c-659df0aad50f.png">





what we need to do is scale our application and the best way to scale our application is just to build multiple service within any infrastructure

In this case how is the client make the request to the server, and which the server will make the request to?


so this can get really complicated and that is why we have NGINX in the middle so instead of the client to worrying exactly where to make the request to, it is just going to make a request  straight to the internet and that is going be caught by NGINX and then the nginx responsabilty to farward that request to any particular server that it chooses and this is typically done by a specific algorithm, and the most commun algorithm is a round robin algorithm where well the first request comes in it just forwards it to this server and then sends it right back, the next request comes in well alrighdy sent it to this one that is 

<img width="660" alt="Screen Shot 2023-03-30 at 2 40 25 PM" src="https://user-images.githubusercontent.com/87101785/228872514-e2c82e8c-8549-4403-8917-783e350d88f7.png">



17: HTTP redirections:
----------------------

17.1: 300 -->

The HTTP 300 Multiple Choices redirect status response code indicates that the request has more than one possible responses. 

17.2: 301 -->

The HyperText Transfer Protocol (HTTP) 301 Moved Permanently redirect status response code indicates that the resource requested has been definitively moved to the URL given by the Location headers. 

recommended to use the 301 code only as a response for GET or HEAD methods


17.3: 302 -->

302 code only as a response for GET or HEAD methods

17.4: 303 -->

303 See Other instead. This is useful when you want to give a response to a PUT method that is not the uploaded resource but a confirmation message such as: 'you successfully uploaded XYZ'.


The HyperText Transfer Protocol (HTTP) 303 See Other redirect status response code indicates that the redirects don’t link to the newly uploaded resources, but to another page (such as a confirmation page or an upload progress page). This response code is usually sent back as a result of PUT or POST. The method used to display this redirected page is always GET.


17.5: 304 -->


The HTTP 304 Not Modified client redirection response code indicates that there is no need to retransmit the requested resources. It is an implicit redirection to a cached resource. This happens when the request method is safe, like a GET or a HEAD request, or when the request is conditional and uses a If-None-Match or a If-Modified-Since header.

17.6: 307 -->

The only difference between 307 and 302 is that 307 guarantees that the method and the body will not be changed when the redirected request is made. With 302, some old clients were incorrectly changing the method to GET: the behavior with non-GET methods and 302 is then unpredictable on the Web, whereas the behavior with 307 is predictable. For GET requests, their behavior is identical.

17.5: 308 -->

308 Permanent Redirect for POST methods instead, as the method change is explicitly prohibited with this status.


NGINX rewrite directive:
------------------------

The return Directive:

You enclose the return in a server or location context that specifies the URLs to be rewritten


18: NGINX command line :
-------------------------


1. Nginx -t 

2. nginx services restart nginx

3. nginx -s reload. ---> (To reload our NGINX configuration)


🌱17. Ressources:
-----------------

https://www.youtube.com/watch?v=auhEJDGHI8Q

https://www.youtube.com/watch?v=2JYT5f2isg4

https://www.youtube.com/watch?v=YqEqjODUkWY&list=PLPUbh_UILtZW1spXkwszDBN9YhtB0tFKC&index=2

https://developer.mozilla.org/en-US/docs/Web/HTTP


https://www.youtube.com/watch?v=iYM2zFP3Zn0

https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server

https://www.youtube.com/watch?v=_0thnFumSdA&t=41s

https://www.digitalocean.com/community/tutorials/understanding-the-nginx-configuration-file-structure-and-configuration-contexts


 
 NGINX FULLCOURSE
 
https://www.youtube.com/watch?v=7VAI73roXaY&t=1022s

NGINX GUID :

https://www.plesk.com/blog/various/nginx-configuration-guide/

Serve static website:


https://docs.nginx.com/nginx/admin-guide/web-server/serving-static-content/


HTTP redirects:

https://www.ohmycrawl.com/technical-seo/301-vs-308/

https://linuxhint.com/nginx-redirect-http-https/#:~:text=Redirect%20HTTP%20to%20HTTPS%20version%20for%20Specified%20domain%20in%20Nginx&text=connections%20specified%20domain.-,Server_name%20domain%2Dname.com%20www.domain%2Dname.,HTTPS%20version%20of%20the%20site.

https://blog.codefarm.me/2021/09/24/http-redirect-3xx/


useful command:
---------------




/Users/souchen/.brew/etc/nginx/nginx.conf

/Users/souchen/.brew/etc/nginx/nginx.conf

nginx -t
