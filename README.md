# ClientServeur-RMI

Rapport sur l'Application RMI de Conversion de Chaînes en Majuscules

1. Interface ServiceRMI

L'interface ServiceRMI définit un service distant qui expose la méthode convertirEnMajuscules. Cette méthode prend une chaîne en argument et renvoie la même chaîne convertie en majuscules. Cette interface joue le rôle de contrat entre le serveur et le client, spécifiant la méthode distante qui peut être appelée.

2. Serveur RMI ServeurRMI

Le serveur RMI, implémentant l'interface ServiceRMI, offre une implémentation concrète de la méthode convertirEnMajuscules. Dans le code du serveur, nous créons un objet Registry sur le port 1099 et enregistrons le stub du serveur avec le nom "ServiceRMI". Le serveur est prêt à accepter les appels distants.

3. Client RMI ClientRMI

Le client RMI se connecte au serveur en utilisant le registre RMI et récupère le stub du service distant. Ensuite, il appelle la méthode distante convertirEnMajuscules avec une chaîne en argument. Le résultat est affiché côté client.
