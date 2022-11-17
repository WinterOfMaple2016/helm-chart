# helm-chart
helm repository, which url is : https://winterofmaple2016.github.io/helm-chart/

# How build a helm repository by GitHub

## 1. Create a new repository
## 2. Clone the GitHub repository
## 3. Create a helm chart
      i.g helm create test
## 4. Package your helm chart
      i.g 
      mkdir docs
      helm package test -d docs/
## 5. Create the index.yaml file for the Helm repository
      i.g helm repo index https://winterofmaple2016.github.io/helm-chart/ .
      Note:
      if you make any further changes in the Helm cahrt. you must regennerate the index.yaml
      file and the .tgz file with the latest changes
## 5. Push changed code to Github repository
      git status
      git add .
      git commit -m "you_commit_message"
      git push
## 6. Create GitHub Pages once the code is pushed to GitHub 
      setting => Pages => Build and deployment =》
      Source：Deploy from a branch
      Branch: target branch: docs
      save it
      
# How use it
## 1. Add Helm repository locaaly
      helm repo add my-repo https://winterofmaple2016.github.io/helm-chart
## 2. Install this Helm chart into your cluster
      helm install <release> myrepo/test -n <namespace> 
