# Mises à jour de la passerelle de pseudonymisation

Paquets de mise à jour **signés** de la passerelle de pseudonymisation de Baracoda AI Labs.

- `version.json` : dernière version publiée et nom du paquet.
- `passerelle-<version>.maj` : paquet signé (Ed25519). La passerelle vérifie la signature à l'installation et à chaque
  démarrage ; un paquet modifié ou non signé est refusé.

Les postes consultent ce dépôt une fois par jour, sauf si l'organisation a réglé sa propre source
(`mises_a_jour.source` : dossier réseau ou adresse interne) ou désactivé les mises à jour.

*Signed update packages for Baracoda AI Labs' pseudonymisation gateway. Packages are verified against the public key
shipped with the installer.*

## Paquets de langue du modèle de détection

`langues/<version du modèle>/langue-<écriture>.npz` : vocabulaire du modèle pour les écritures autres que l'alphabet
latin (cyrillique, grec, arabe, hébreu, chinois…). La passerelle ne télécharge un paquet que lorsqu'un document
contient cette écriture, et vérifie son empreinte contre la liste livrée avec l'application. Une organisation peut
les déposer d'avance dans son propre dossier réseau (réglage `langues.source`) et couper le téléchargement.
