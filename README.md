# test-projet2

# lancement du script sur une machine distante
  # fonction pour lire le nom de la machine distante

nommachine() { 

read -p "Entrez l'ip de la machine sur lqauelle vous souhaitez lancer le script?" nommachine
echo "$nommachine"
}

  # fonction pour le chemin serveur/hote

execute_remote_script() { 
read -p "quel est l'utilisateur de la machine distante?" remoteuser
read -p "entrez le path du script que vous souhaitez lancer" remotescript

ssh "$remoteuser@$nommachine" 'bash -s' < "$remotescript"
 }

   
