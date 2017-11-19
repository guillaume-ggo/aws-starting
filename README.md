#Gestion des instance EC2 avec AWS CLI
##TODO Création d'utilisateur IAM
##TODO Générer une paire de clés
##Configurer les appels à l'API AWS
* Exécuter la commande interactive `aws configure`en utilisant une AWS Access Key et une AWS Access Secret valide
##TODO Création d'une instance
##Ajout d'une règle de sécurité à un groupe existant
'''
aws ec2 authorize-security-group-ingress --group-name <group_name> --protocol tcp --port 22 --cidr $(curl ipinfo.io/ip | tr -d "[:space:]")/24
'''
##Connexion  à une instance
* S'assurer que le fichier de clé a un accès restraint `chmod 400 <nom_fichier_key_pair.pem>
* Se connecter comme suit: `ssh -i <nom_fichier_key_pair.pem> ec2-user@ec2-ip.region.compute.amazonaws.com`


