## Dev

1. Clone the repository
2. create .env file based on .env.template
3. Run `docker-compose up --build`
  

### Steps to create a new submodule


1. Create a new repository in GitHub
2. Clone the repository in your local machine
3. Add the submodule, where `repository_url` is the url of the repository and `directory_name` is the name of the folder where you want to save the submodule (it should not exist in the project)
```
git submodule add <repository_url> <directory_name>
```

4. Add the changes to the repository (git add, git commit, git push)
```
git add .
git commit -m "Add submodule"
git push
```

5. Initialize and update Submodules, when someone clones the repository for the first time, they must run the following command to initialize and update the submodules
```
git submodule update --init --recursive
```

6. To update the references of the submodules
```
git submodule update --remote
```


## Important

> [!CAUTION] 
> If you are working in the repository that has the submodules, **first update and push** in the submodule and **then** in the main repository.
> 
> If you do it the other way around, you will lose the references of the submodules in the main repository and you will have to resolve conflicts.

