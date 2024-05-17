Projet d'installation de Semaphore avec Ansible sur Google Cloud Platform par Paul CACHERA
Ce projet vise à automatiser le déploiement et la configuration de l'outil Semaphore sur une machine virtuelle Google Cloud Platform (GCP) à l'aide d'Ansible.

Structure du projet
Le projet est structuré de la manière suivante :

my-project/
├── ansible/
│   ├── roles/
│   │   └── semaphore_install/
│   │       ├── defaults/
│   │       │   └── main.yml
│   │       ├── tasks/
│   │       │   └── main.yml
│   │       └── vars/
│   │           └── vault.yml
│   ├── install_semaphore.yml
│   ├── hosts.ini
│   └── ansible.cfg
├── terraform/
│   ├── main.tf
│   ├── outputs.tf
│   └── variables.tf
└── .gitignore

Déroulement du projet
Déploiement de la VM GCP avec Terraform :

Utilisation de Terraform pour déployer une machine virtuelle Debian sur Google Cloud Platform dans la région eu-west3.

Configuration d'Ansible :

- Mise en place d'un inventaire Ansible (hosts.ini) pour spécifier l'adresse IP de la VM GCP.
- Configuration d'un playbook Ansible (install_semaphore.yml) pour installer et configurer Semaphore sur la VM.

Installation de Semaphore avec Ansible :

- Utilisation du rôle Ansible semaphore_install pour télécharger et installer Semaphore.
- Configuration de Semaphore avec les variables définies dans vars/vault.yml.

Exécution du playbook :

- Exécution du playbook Ansible avec la commande ansible-playbook install_semaphore.yml -i hosts.ini --ask-vault-pass.

Réussites
1. Déploiement réussi de la VM GCP avec Terraform.
2. Installation et configuration réussies de Semaphore sur la VM avec Ansible.
3. Utilisation des variables chiffrées avec Ansible Vault pour sécuriser les informations sensibles.

Problèmes rencontrés
1. Permissions insuffisantes pour exécuter certaines tâches Ansible en tant qu'utilisateur non privilégié.
2. Problèmes avec les permissions lors de l'initialisation de la configuration Semaphore.
3. Échec de la résolution du problème des permissions avec les méthodes alternatives proposées.

Problème non résolu
1. Le problème des permissions lors de l'initialisation de la configuration Semaphore n'a pas été résolu.

Merci de m'avour lu et bon week-end bg 🍻







