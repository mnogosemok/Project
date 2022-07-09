* ## Project

 ![Image 1](installed-joomla.PNG)
 ![Image 1](slack-notification.PNG)
* ## Jenkins Shell
``` bash
#!/bin/bash
if [ -d "Project" ]; then
  git pull
  ansible-playbook /var/lib/jenkins/workspace/MyProject/Project/Playbook/joomla.yaml -i /var/lib/jenkins/workspace/MyProject/Project/Playbook/inventory.yaml
else
   git clone https://github.com/mnogosemok/Project.git
   ansible-playbook /var/lib/jenkins/workspace/MyProject/Project/Playbook/joomla.yaml -i /var/lib/jenkins/workspace/MyProject/Project/Playbook/inventory.yaml
fi
```

