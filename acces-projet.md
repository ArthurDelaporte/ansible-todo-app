
# Lancer les playbooks Ansible

Ce guide explique comment exécuter les playbooks Ansible pour déployer l'application Todo-PHP.

---

## **Prérequis**
1. **Outils nécessaires :**
    - Ansible installé (documentation officielle : [Ansible Installation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)).
    - Clé SSH pour accéder au serveur distant.
    - Fichiers : `application.yml` et le dossier `files`.

---

## **Étapes pour exécuter les playbooks**
1. **Cloner le dépôt Git :**
   ```bash
   git clone https://github.com/ArthurDelaporte/ansible-todo-app.git
   cd ansible-todo-app
   ```

2. **Lancer le playbook principal :**
   ```bash
   ansible-playbook -i inventory application.yml
   ```

3. **Vérifiez que toutes les tâches ont été effectuées sans erreur.**

---

## **Dépannage**
- Si une tâche échoue, utilisez le mode de vérification Ansible :
  ```bash
  ansible-playbook -i inventory application.yml --check --verbose
  ```
- Assurez-vous que le serveur distant est accessible via SSH.
