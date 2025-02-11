https://github.com/didier-mycontrib/msa-vagrant/with-wsl2/install-docker.sh
si besoin d'installer docker et docker compose sur Ubuntu (ex: sur wsl2)
--------------
tutorial "jenkins+python" : https://www.jenkins.io/doc/tutorials/build-a-python-app-with-pyinstaller/
repo officiel : https://github.com/jenkins-docs/quickstart-tutorials
============
résumé sur commandes à lancer:

git clone https://github.com/jenkins-docs/quickstart-tutorials
cd quickstart-tutorials
sudo docker compose --profile python up -d
sudo docker compose ps
http://localhost:8080 et login via admin/admin
nouvel item de type pipeline et de nom simple-python-pyinstaller-app (save)
configuration: 
 pipeline/definition/Pipeline script from SCM 
 via GIT
 repo url : https://github.com/didier-tp/simple-python-pyinstaller-app
  branch : */main plutôt que */master
(save config)
Lancer un build 
...
sudo docker compose --profile python down -v --remove-orphans
  
