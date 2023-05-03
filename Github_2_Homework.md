GitHub. HW_2
1. На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bag Reports
- SQL
- Charles
- Mobile testing

>mkdir git_branchig
>Create new repository Git_Branching in Github
>cd git_branching
>git clone git@github.com:VukulyaSergeeva/Git_Branching.git
 
>git branch Postman
>git branch Jmeter
>git branch CheckLists
>git branch Bag_Reports
>git branch SQL
>git branch Charles
>git branch Mobile_testing


2. Запушить все ветки на внешний репозиторий

>git push origin --all

3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта

>git checkout Bag_Reports
>cat > bug_reports_attributes.txt

>Structure of bag report:
>1.Id
>2.Severity
>3.Priority
>4.Title
>5.Enviroment
>6.Precondition
>7.Step to reproduce
>8.Actul result
>9.Ecpected result
>10.Attachment
>11. Post condition
>12.Reproducibility

4. Запушить структуру багрепорта на внешний репозиторий
>git add .
>git commit -m "create bug_reports_attributes.txt"
>git push 

5. Вмержить ветку Bag Reports в Main

> git checkout main
>git merge Bag_Reports


6. Запушить main на внешний репозиторий.

>git add .
>git commit -m "added file from bug_reports branch"
>git push

7. В ветке CheckLists набросать структуру чек листа.
>git checkout CheckLists
> cat > checklist.txt
>1Id
>2Title
>3Environment
>4Precondition
>5Inputs
>6Step to reproduce
>7Expected result
>8Actual result
>9Status
>10 Attachment

8. Запушить структуру на внешний репозиторий
>git add .
>git commit -m "create Checklist.txt"
> git push 
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main
10. Синхронизировать Внешнюю и Локальную ветки Main
>git pull
