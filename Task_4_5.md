in task 4  
cd path/to/MRM_DarrenPais          # Navigate to your repo
git checkout -b Temp               # Create and switch to the Temp branch
echo "# Task 3: Upload CSV File" > Task_3.md  # Create the README file
echo "In Task 3, a CSV file was downloaded and uploaded to the GitHub_task folder." >> Task_3.md
echo "" >> Task_3.md
echo "## Git Commands Used:" >> Task_3.md
echo "1. git add <file>" >> Task_3.md
echo "2. git commit -m 'Added CSV file to GitHub_task folder'" >> Task_3.md
echo "3. git push https://<your_actual_PAT>@github.com/MRM-AIA-TP-2026/MRM_DarrenPais.git" >> Task_3.md
git add Task_3.md                  # Stage the new file
git commit -m "Add Task_3.md README file for Task 3"  # Commit the changes
git push -u origin Temp            # Push the Temp branch to GitHub

in task 5 
git checkout main                                # Switch to the main branch
git merge Temp                                   # Merge Temp into main
git push origin main                             # Push merged changes to GitHub
echo "# Task 4 and 5: Merge Branches" > Task_4_5.md  # Create the README file
echo "In Task 4, a branch named Temp was created and a README file named Task_3.md was added." >> Task_4_5.md
echo "In Task 5, the Temp branch was merged into the main branch." >> Task_4_5.md
echo "" >> Task_4_5.md
echo "## Git Commands Used:" >> Task_4_5.md
echo "1. git checkout main" >> Task_4_5.md
echo "2. git merge Temp" >> Task_4_5.md
echo "3. git push origin main" >> Task_4_5.md
git add Task_4_5.md                              # Stage the new README file
git commit -m "Add Task_4_5.md README file for Tasks 4 and 5"  # Commit the changes
git push origin main                             # Push the README file to GitHub
