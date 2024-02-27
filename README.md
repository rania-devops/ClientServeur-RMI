# ClientServeur-RMI

Rapport sur l'Application RMI de Conversion de Chaînes en Majuscules

1. Interface ServiceRMI

L'interface ServiceRMI définit un service distant qui expose la méthode convertirEnMajuscules. Cette méthode prend une chaîne en argument et renvoie la même chaîne convertie en majuscules. Cette interface joue le rôle de contrat entre le serveur et le client, spécifiant la méthode distante qui peut être appelée.

2. Serveur RMI 

Le serveur RMI, implémentant l'interface ServiceRMI, offre une implémentation concrète de la méthode convertirEnMajuscules. Dans le code du serveur, nous créons un objet Registry sur le port 1099 et enregistrons le stub du serveur avec le nom "ServiceRMI". Le serveur est prêt à accepter les appels distants.

3. Client RMI 

Le client RMI se connecte au serveur en utilisant le registre RMI et récupère le stub du service distant. Ensuite, il appelle la méthode distante convertirEnMajuscules avec une chaîne en argument. Le résultat est affiché côté client.

***** Vérification de la Génération des Souches dans un Programme RMI *****

La détermination de la méthode de génération des souches dans un programme RMI peut être effectuée en examinant le processus de compilation. 

Si aucune référence explicite à l'outil rmic n'est présente dans ce processus, il est probable que les souches soient générées automatiquement par le runtime Java lors de l'exécution.

Lorsqu'une génération explicite des souches est effectuée, un appel à rmic est inclus dans le processus de compilation avec une commande telle que :  rmic ServeurRMI

Cependant, si aucune mention de rmic n'est observée pendant la compilation, le système RMI génère probablement les souches de manière implicite lors de l'exécution.

La génération implicite des souches est une fonctionnalité pratique du runtime RMI, simplifiant le processus pour les développeurs en automatisant la création des classes de stub. Ainsi, même en l'absence d'appels directs à rmic pendant la compilation, le système RMI prend en charge la génération des souches au moment de l'exécution. La compréhension de ces nuances facilite la détermination du mode de génération des souches dans un contexte RMI spécifique.
