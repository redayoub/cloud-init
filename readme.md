# cloud-init

## definition du besoin

Il s'agîrait d'installer et de configurer cloud-init pour un système debian/buster qui fonctionneraît dans AWS/ec2 

doc metadata outscale : https://wiki.outscale.net/display/EN/Accessing+the+Metadata+and+User+Data+of+an+Instance

A configurer via cloud-init :

- Les clés SSH pour l'utilisateur "debian"
- le hostname
- récupérer un "TAG" et l'écrire dans un fichier /tmp/value.txt (voi tags/KEY_NAME dans la doc outscale ci-dessus)

Au préalable l'user debian sera déjà créé dans l'image debian.

Attention à rendre le rôle : idenpotent, indépendant et tester avec molecule.

Conseil : ne pas partir d'un rôle déjà fait depuis ansible-galaxy

Pour tester dans molecule (vagrant) il existe un projet qui pourrait aider à simuler les metadata : https://github.com/craighurley/vagrant-cloud-init
