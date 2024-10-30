went to desktop directory - cd desktop
cloned mrm repo here -  git clone https://github.com/MRM-AIA-TP-2026/MRM_DarrenPais.git
opened cloned repo - cd MRM_DarrenPais
created folder in it , opened it ,added a python file and went back to high directory MRM_DarrenPais - mkdir GitHub_task
  cd GitHub_task
  echo 'print("Hello World!")' > hello_world.py
  cd ..
staged the folder for commit - git add GitHub_task
commiting the changes - git commit -m "Added GitHub_task folder with Hello World program"
push the changed onto github using PAT - git push https://<your_actual_PAT>@github.com/MRM-AIA-TP-2026/MRM_DarrenPais.git
