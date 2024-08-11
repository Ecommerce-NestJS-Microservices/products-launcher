# Dev

1. Clone repository
2. Create an `.env` based in the `.env.template`
3. Execute the command `git submodule update --init --recursive` to rebuild the modules.
3. Execute command `docker compose up --build`


### Steps to create Git Submodules

1. Create un new repository in GitHub.
2. Clone repository in local machine.
3. Add  submodule, where `repository_url` es la url del repository and `directory_name` is the name of folder where you want saved the sub-module (The project should not exist)
```
git submodule add <repository_url> <directory_name>
```
4. Add changes at repository (git add, git commit, git push)
Ej:
```
git add .
git commit -m "Add submodule"
git push
```
5. Initialize and update Sub-modules, when someone clone the repository for first time, It should execute the following  command to initialize and update the sub-modules
```
git submodule update --init --recursive
```
6. To update the references of the  sub-modules
```
git submodule update --remote
```


## Important
If you work in the repository that contains the  sub-modules, **first update and push** in the  sub-module and **then** int the main repository. 

I you do it the other way around, you will lose the submodules  references int the main repository and will have to resolve conflicts.






